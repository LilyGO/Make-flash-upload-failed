# Make-flash-upload-failed
TTGO ESP32-IDF-esptool.py

This repository is to solve ESP32 development board can not upload the problem, I hope 
to solve your problem. If you have a poor description or we do not understand clearly, 
please leave a message below. I will reply as soon as possible

ESP-idf Environment to build:https://github.com/espressif/esp-idf

# Note1:Connect your device.

Under linux, all devices are files. 
Especially in the virtual machine running linux system, linux system and windows system will "snatch" your device.
Of course, this does not matter when program compilation is "make." However, when you execute "make flash", the following occurs.
![image](https://github.com/LilyGO/Make-flash-upload-failed/blob/master/image/image1.png)

And we only need to click on this option (U disk, removable hard disk are here to turn the device on and off)
![image](https://github.com/LilyGO/Make-flash-upload-failed/blob/master/image/image2.png)
This time we can read the connected device

# Note2:Give permission

Next, we improve the next link. Right, before that. We must first check whether the development board connected 
to the device. 
   @ls / dev / ttyUSB *
![image](https://github.com/LilyGO/Make-flash-upload-failed/blob/master/image/image3.png)

If there is "no such file or directory", then please check your USB data cable and computer port and whether 
the implementation of the Note1 operation.
Because all devices are files, you have to upload your program to your device, you must give it read and write 
permissions. sudo can temporarily gain administrator privileges. Enter the following: 
   
@sudo chmod 777 / dev / ttyUSB0 (device name based on the device you read to prevail, but most are ttyUSB0)


![image](https://github.com/LilyGO/Make-flash-upload-failed/blob/master/image/image4.png)


