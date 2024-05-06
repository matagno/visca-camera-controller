# Program for controlling a Sony EVI-D70/D70P camera

[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/Tisma09/ProjetCamera/blob/main/README.md)
[![fr](https://img.shields.io/badge/lang-fr-blue.svg)](https://github.com/Tisma09/ProjetCamera/blob/main/README.fr.md)

This program allows for controlling a camera using the VISCA protocol along with the RS-232 communication standard.

The supported commands enable the camera to be oriented in all directions. These commands are located in the `CameraVisca.h` and `CameraVisca.cpp` files and can be modified using the VISCA commands listed in [this manual](https://www.audiogeneral.com/Sony/evid70_manual.pdf).

Depending on the camera configuration (whether it is intended to be mounted upside down or not), it is possible that the directions may be inverted.

##  ➤ Supported Device
- Windows
- Arduino Mega
        

## 🛠️ Installation and Dependencies

### Windows 

- CMake or an IDE supporting CMake


### Arduino

- Arduino IDE or an IDE supporting Arduino SDK (e.g., Visual Studio with the vMicro extension)
        
## 🧑🏻‍💻 Usage

### For Windows 

In `SerialPC.hpp`, check and redefine if necessary the COM port number being used. You can find this number in the Device Manager.

```
static const char* device = "\\\\.\\COM6"; // Définition du port 
```
You can now compile and run the program using CMake or any development environment that includes CMake.

Control is done using the ZQSD keys. You can now control the camera!

### For Arduino

In `KeyboardArduino.hpp`, check and redefine if necessary the pins corresponding to the connections of your buttons (currently configured for Up: pin 52, Down: pin 46, Right: pin 50, Left: pin 48).

Open `ProjetCamera.ino` in Arduino IDE or another IDE capable of uploading a program to your Arduino.

Upload the code. You can now control the camera!
