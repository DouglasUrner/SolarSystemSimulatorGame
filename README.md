# Solar System Simulator Game

A simulation of our Solar System and a game at the same time made mainly for educational purposes (it gives a good sense of the time and space scale of out Solar System). The planets, the moon, and the Space Craft follow realistic (elliptical) orbits in phase space and the relative sizes of planets and moon are correct.

For the orbital elements of the planets I used values from the NASA planetary fact sheet. The radius of the planets and the Earth's moon are increased by a factor of 30 to avoid floating point errors since the GPU is using single precision arithmetic internally. The planetary orbits are pre-computed at start time using a 4th-order Runge-Kutta integrator. Specifically the 2nd Kepler-law (which is a differential equation) is solved for the values according to the NASA Fact Sheet for the planets of our solar system and the moon.

The trajectories of the Space-Craft are calculated at run time using a 2nd order Leapfrog Integrator with initial conditions based on user input and Earth's position and velocity at the time of launch. The goal of the game is to launch Space Craft and complete the missions.

Check out the video for gameplay footage. Note that in order to play the game you need a mouse with a wheel.

Programmed in C# and powered by Unity. 
