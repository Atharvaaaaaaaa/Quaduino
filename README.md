**Course Name: Electronics in Service to Society (R4EC30116L)**

**Date: January-May 2023**


# Quaduino

Quaduino is a self-levelling Arduino Uno based quadcopter drone.

## Table of Contents

- [About the Project](#about-the-project)
    - [Aim](#aim)
    - [Description](#description)
- [Getting Started](#getting-started)
    - [Components](#components)
    - [Tech Stack](#tech-stack)
    - [Software](#software)
- [Theory and Approach](#theory-and-approach)
- [Future Work](#future-work)
- [Troubleshooting](#troubleshooting)
- [Contributors](#contributors)
- [Acknowledgements and Resources](#acknowledgements-and-resources)

## About The Project

### Aim

Develop a self-levelling quadcopter using Arduino Uno as a flight controller and interfacing it with components such as motors, ESCs, etc.

### Description
Quadcopter is an unmanned aerial vehicle (UAV) or drone with four rotors, each with a motor and propeller. A quadcopter can be manually controlled or can be autonomous. It belongs to a more general class of aerial vehicles called multicopter or multirotor.


## Getting Started

### Components

- 450 size Quadcopter Frame
- 4 x 1000kV motor, 10x4.5 propellers and 30A ESC Combo
- 3S, 2200 mAh, 30C, 11.1V Lipo Battery
- Arduino Uno
- MPU 6050 Gyroscope + Accelerometer
- Flysky fs-i6x Transmitter paired with fs-iA10B Receiver
- OV7670 CMOS VGA Camera Module
- Resistors- 1k, 1.5k, 330 ohms
- 1N4007 1A Diode
- Some LEDs, Jumper Wires, etc

### Tech Stack
- Embedded C
- C++

### Software
- Protues 8  
- Arduino IDE

## Theory and Approach

### Build process

We start with assembling the drone starting with the frame. The first step is to mount the motors and the ESCs onto the frame. Then mount the electronic components, make the appropriate connections and connect it to computer for programming.

![CircuitDiagram](https://github.com/cp2392/Quaduino/assets/88549231/b94bad4f-453b-4b8c-8fc2-7ac5a9142d59)

The Arduino on the drone requires three codes to be flashed onto it:
- Setup: where we initialize the Arduino Uno for the quadcopter code and set up and calibrate the MPU 6050 sensor
- ESC Calibration: This is the most important step as it makes sure the motors are spinning in accordance with each other, and finally
- Flight Controller: This program loads the actual flight control data onto the Arduino and after this step, the drone is ready to fly. 

### How does a drone work?

![MotorDirection](https://github.com/cp2392/Quaduino/assets/88549231/5385e541-00bf-436e-8969-089a9d839d76)

Quadcopters make use of 4 Motors. Two of these motor spin clockwise while the other two spin counterclockwise. Motors on the same axis spin in the same direction, as illustrated here. It uses the basic principle of Newton’s Third Law of motion by pushing the air opposite to the direction of desired motion and moving around.

![BuildPhoto1](https://github.com/cp2392/Quaduino/assets/88549231/728d1f92-f8b7-4bda-95c7-241bae49a82d)    ![BuildPhoto2](https://github.com/cp2392/Quaduino/assets/88549231/26dbbf59-c4b6-4978-8667-18de24c5a44d)


## Results and Demo
The result of this was a functional quadcopter with decent flight capabilities and auto-levelling. 

![FinalBuild](https://github.com/cp2392/Quaduino/assets/88549231/9d99b93c-1676-4217-9166-200b285d8cf6)


## Future work
In the future we plan on adding a GPS module over it so that it can automatically land based on satellite signals.
We also plan on mounting a proximity sensor on either side of the quadcopter so that it does not crash along walls by quickly moving away from them.
And other similar things such as a Barometer, a Gimbal and Compass would be added to the quadcopter to enhance its utility.


## Troubleshooting

The motors while spinning might suddenly stop mid-flight and the calibration is lost. Due to this reason, restrict the quadcopter to a maximum flight time of 2 minutes in order to look for safety and not to damage the frame. 
This can be tackled by using a higher capacity battery and high quality motors with low power consumption.


## Contributors

- [Chirag Patil](https://github.com/cp2392)
- [Yash Deshpande](https://github.com/yashLM705)
- [Atharva Bendre]
- [Shreyas Bhatlawande]

## Acknowledgements and Resources

- [Joop Brokking’s YMFC-3D](http://www.brokking.net/ymfc-al_main.html)
- [Joop Brokking’s Video Tutorials](https://www.youtube.com/watch?v=XFxqFQwRumc&list=PL0K4VDicBzsibZqfa42DVxC8CGCMB7G2G&pp=iAQB)
- [Swapnil Nimbalkar’s Arduino Drone](https://www.youtube.com/watch?v=zLdw0reI86o)
