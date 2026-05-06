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

# Routing
![image](https://stasis.hackclub-assets.com/images/1777234165503-dxfk10.png)

# PCB Render
![img](https://stasis.hackclub-assets.com/images/1777153572868-ibuv46.png)

# BoM
The BoM can be found in the Project-files folder or on [My stasis page](https://stasis.hackclub.com/dashboard/discover/cmodeeflm011401mx99b0l96k)


# Making process
This is a copy of my stasis journals.

## 5/5/2026 8 PM - Correcting the repo

_Time spent: 0.15h_

This was a really small change , i updated the media and README , added the journals , and thats basically everything. I hope the repo is fine now , as i don't see what else could be updated. 
![image](https://stasis.hackclub-assets.com/images/1778011435365-fr66z8.png)

## 4/27/2026 2 PM - Creating Github repo

_Time spent: 1h_

### Problems with git
I struggled with this wayy to much since at first i wanted to use git on my laptop which did not work , after i spent way too much time on this i found out that the Arch User Repository has a linux version of GIthub Desktop (I use arch btw) so i downloaded that and started working on the repo.
### Creating the repo
I copied in all the files , added the schematic to README.md  , made a description of all the parts in the schematic and added the BoM
![2026-04-27_16-25-43](https://stasis.hackclub-assets.com/images/1777300854292-i6ncoi.png)



## 4/26/2026 8 PM - Fixing the pcb.

_Time spent: 0.25h_

Today i realized that the automatic traces won't be enough to carry the current of 1-2A which the stepper motor will need , it was a quick fix that saved me a lot of time and money
![image](https://stasis.hackclub-assets.com/images/1777234165503-dxfk10.png)



## 4/26/2026 4 PM - Designing the actual PCB

_Time spent: 2.5h_

Yesterday i started working on turning the schematic into an actual PCB. At first i wanted to make it the same size as the Pi but while all the components did fit , routing them wasn't possible. Finally , i decided to make the board 86mmx57mm and everything was able to fit with some room left  over. After everything was placed and routed , i labeled all the ports and pins. I also added a cool logo in the corner for looks.
After all of that was done i made sure that all connections were correct.
![pcb](https://stasis.hackclub-assets.com/images/1777221774224-g265nn.png)



## 4/25/2026 4 PM - Deciding on what the board should have, making the schematic.

_Time spent: 2h_

## Deciding the boards functions and compnonents
### The functions
I decided that the board will have:

-The ability to control 2 stepper motors

-2 I2C ports for screens and other I2C Devices

-2 Ports for digital sensors

### The parts
To fulfill these requirements i decided on these parts:

-2 A4988 Stepper Motor controllers , since they are pretty simple , cheap and small while also having enough power for most stepper motors.

-4 JST 2.0 4pin connectors for I2C and the steppers.

-2 JST 2.0 3pin connectors for the sensors.

-A 3.5mm barrel jack for powering the motors.

### Making the schematic
This was pretty straight forward , and involved looking at the part's documentation , deciding the GPIO's which i wanted to use and drawing these connectons.
![schematic](https://stasis.hackclub-assets.com/images/1777133171479-8eew2k.png)

