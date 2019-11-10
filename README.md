# Solar System Simulator Game

<iframe width="560" height="315" src="https://www.youtube.com/embed/1qL-AhrCbQ8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

A simulation of our solar system and a game at the same time made primarily for educational purposes (it gives a good sense of the time and space scale of out Solar System). The planets, the moon, and the space craft follow realistic (elliptical) orbits in phase space and the relative sizes of planets and moon are correct.

For the orbital elements of the planets I used values from the [NASA Planetary Fact Sheet][2]. The radius of the planets and of the Earth's moon are increased by a factor of 30 to avoid floating point errors since the GPU is using single precision arithmetic internally. The planetary orbits are pre-computed at start time using a 4th-order [Runge-Kutta][1] integrator. Specifically Kepler's 2nd law (which is a differential equation) is solved for the values according to the NASA Fact Sheet for the planets of our solar system and the moon.

The trajectories of the space craft are calculated at run time using a 2nd order [Leapfrog][3] integrator with initial conditions based on user input and Earth's position and velocity at the time of launch. The goal of the game is to launch space craft and complete the missions.

Check out the video for gameplay footage. Note that in order to play the game you need a mouse with a wheel.

Programmed in C# and powered by Unity. 

[1]: <https://en.wikipedia.org/wiki/Runge–Kutta_methods>
[2]: <https://nssdc.gsfc.nasa.gov/planetary/factsheet/>
[3]: <https://en.wikipedia.org/wiki/Leapfrog_integration>
