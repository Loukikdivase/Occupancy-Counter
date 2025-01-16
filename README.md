# Occupancy Counter

by: Loukik-Sachin Divase, Rudy Marvyn Kalisetty-Appadu


**Faculty of Technology and Bionics**

***Rhine-Waal University of Applied Sciences***

Date: 16 January 2025

----

## Abstract

The occupancy counter is designed to ensure a seamless flow of people, especially on a busy day. The system tracks the number of people entering and exiting a room and can be used for libraries, offices, toilets, labs, and more. It features real-time monitoring, status indication using LEDs, compliance with safety regulations, and energy-efficient operation. A microcontroller with IR sensors detects directional movement, updates the LCD display accordingly.

## Table of Contents

[[_TOC_]]

## 1 Introduction

Managing space efficiently in crowded environments can be challenging. The people counter helps address this issue by providing real-time tracking of room occupancy.

## 2	Theory

The occupancy counter relies on IR sensors to detect movement direction. The system uses logic to determine whether a person enters or exits, ensuring accurate count tracking. If a person passes through sensor 1(placed outside the room near the door) and sensor 2(placed inside the room near the door), the sensor will count. The sensor will increase the count by 1 if a person passes sensor 1 before sensor 2. The sensor will decrease the count by 1 if the person passes sensor 2 before sensor 1.

## 3	Methodology

### 3.1 Hardware

The system consists of:  
•	Microcontroller (ATmega328p) for processing  
•	16MHz Crystal Oscillator  
•	Infrared LED and photodiode for movement detection  
•	LCD display (16x2) to show real-time occupancy count  
•	Buzzer for alerts when a room reaches maximum capacity  
•	LED indicators (Red/Green/Yellow) for status display  
•	9V lithium battery for power supply  
•	Voltage regulator (LM7805) for power management  
•	Comparator (LM393) for signal processing  
•	resistors  
•	capacitors  
•	inductor  
•	switches  

### 3.2 Software

•	Notepad++ for writing the main program  
•	myAVRboard MK2 for flashing the ATmega328p microcontroller  
•	The program tracks occupancy using IR sensor logic and updates the display accordingly.  

#### Code Snippets

//Reset lock for sensor 1 when signal goes HIGH  

if (sensor1_state && sensor1_locked)  
{  
     sensor1_locked = 0; //Reset lock  
}
            
//Reset lock for sensor 2 when signal goes HIGH  

if (sensor2_state && sensor2_locked)  
{  
     sensor2_locked = 0;  // Reset lock  
}  

## 4	Results

### Prototype

### 4.1 Schematic

![alt text](resources/images/v1_schematic.png "Schematic")

### 4.2 board

![alt text](resources/images/v1_top.png "top")

![alt text](resources/images/v1_bottom.png "bottom")

### 4.3 UV Masking

![alt text](resources/images/uvmask.jpg "uvmask")

### 4.4 Etching

![alt text](resources/images/sodiumhydroxide_solution.jpg "sodiumhydroxide_solution")

![alt text](resources/images/etching.jpg "etching")

![alt text](resources/images/etching1.jpg "etching1")

![alt text](resources/images/etched_pcb.jpg "etched_pcb")

### 4.5 Drilling

![alt text](resources/images/drilling.jpg "drilling")

### 4.6 Baking

![alt text](resources/images/baking.jpg "baking")

### 4.7 Testing

![alt text](resources/images/testing.jpg "testing")

![alt text](resources/images/testing1.jpg "testing1")

### 4.8 Outsourcing

![alt text](resources/images/outsourcing.jpg "outsourcing")

## version 2 (additional)

### Schematic

![alt text](resources/images/v2_schematic.png "v2_Schematic")

### Board

![alt text](resources/images/v2_top.png "v2_top")

![alt text](resources/images/v2_bottom.png "v2_bottom")

## 6	Discussion

The system performs well in controlled conditions. However, environmental factors such as lighting variations may affect sensor accuracy. Calibration is necessary for optimal performance.

What exactly happens? 
The person must pass both sensors to register the count since our product is directional.

## 7	Concluding Comments

As aspiring engineers, we believe that this project was a success. However, there might be some unsolved challenges that we did not encounter, and we would be more than happy to address them in the future. Future work could involve integrating wireless data transmission for monitoring remotely.

## 8	Power Consumption

Total power consumption: 1.29W, where V = 6V and I = 0.22A

Actual useful power consumption: 1W,  where V = 4.85V and I = 0.21A.

## 9	References

* [1] https://shop.myavr.de/Systemboards%20und%20Programmer/myAVR%20Board%20MK2,%20best%C3%BCckt.htm?sp=article.sp.php&artID=40

* [2] https://docs.arduino.cc/hardware/uno-rev3/

* [3] https://github.com/Loukikdivase/Occupancy-Counter/tree/main/resources
