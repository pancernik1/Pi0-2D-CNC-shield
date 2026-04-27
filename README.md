# Goal
This is a sideproject i made for Hackclub Stasis, it aims to make the raspberry pi zero a viable option for 2D CNC by giving it the ability to control 2 stepper motors , 2 I2C devices and connect 2 digital sensors (although you can also connect servos or other devices that run on 3.3V digital signals)
# Schematic
![schematic.png](https://github.com/pancernik1/Pi0-2D-CNC-shield/blob/13eeaab1e8e6314a44f4f6d6375c262eb7c1fe1f/Media/schematic.png)

## Part Descriptons
|NAME      |FUNCTION  |
|:---------|:---------|
|U2|The A4988 chip that controls stepper 1|
|U1|The A4988 chip that controls stepper 2|
|DC1|Supplies 8-35V to the A4988 chips|
|RPi|Here you can eithers solder in the Pi or a 2x20 2.54mm female connector|
|STEP 1|JST connector for stepper 1|
|STEP 2|JST connector for stepper 2|
|I2C-1|JST connector for I2C device|
|I2C-2|JST connector for I2C device|
|SENS-1|JST connector for connecting sensors/other GPIO devices|
|SENS-2|JST connector for connecting sensors/other GPIO devices|
