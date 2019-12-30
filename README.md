# AlphaBot2_motion_opencv
A little project in C -with a bit of C++ for the OpenCV bit, moving around an Alphabot2 mini robot. The hardware is an AlphaBot2 Raspberry Pi Zero W based mini robot. My main motivation while doing it was of self-educating myself, also I was a bit fed up of finding Python only code for something that is -by definition- a real time application on a limited resources system e.g. a Raspberry Pi.

All the code is into a monolithic C++ file (mostly C really) using OpenCV for motion detection and all the interaction with the GPIO is made by using the pigpio library, which works great by the way.
The robot basically stays put waiting for something to move in front of the camera to start driving around itself for a random number of seconds, while avoiding obstacles using its ultrasounds sensor and a couple of infrared proximity sensors. Now to be fair, reaction to movement is sloooow, this is due to the lack of processing power of the zero, it should be much better with a PI 3 and obviously the new model 4.

The code itself is quite robust but it could be sort of translated/improved/made more elegant and more 'C++ ish', there are abundant comments all over the place to explain what is going on, which I really appreciate when reading somebody else's.

It assumes that OpenCV and pigpio are installed and working. To enable an easy compiling, I also include an .sh file with the right compilation parameters to the g++ compiler: motioncv_compiling.sh.

That's it.
