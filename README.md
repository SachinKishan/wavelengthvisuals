# wavelengthvisuals

A simple color data visualiser which takes wavelength values, converts it into CIE XYZ 1931 color space and then converts that into sRGB color space and displays it on the screen. 

It's limited right now since I'm only taking integer wavelength values as input so it's not a very varied color palette. 

Demo:

https://github.com/SachinKishan/wavelengthvisuals/assets/33657481/8deed6b3-a4f0-4bda-a96f-b704f24deb2b




# Installation instructions
You will need CMake to run this project.

1. Clone the repository
2. Create a new folder called 'build'.
3. In the repository, open the command line or any terminal.
4. Type
```
cd build
```
5. Type
```
cmake ..
```
6. Type
```
cmake --build .
```
7. Open the created visual studio project solution colordatareader.sln
8. The project should open and work on machine as intended. In case you get an error such as "ACCESS DENIED", try changing the Startup Project
9. The project should work as intended
