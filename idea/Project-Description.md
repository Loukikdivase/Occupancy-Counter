# Project title
	- Occupancy counter
	
## Project overview
	- The occupancy counter is designed to keep seemless flow whenever there's a high increase in people on a busy day. 
	- Also, the system is designed to track the number of people entering and exiting a room.
	- This type of system is beneficial for library, offices, toilets, labs, etc. 

### Main features

	• Room management: 
	- By providing real-time data on room occupancy, this system helps in managing room usage.
	
	• Status LED: 
	- Whenever the room is full, the status LED - Red LED will light on depending on the number of spaces being occupied inside. 
	For example:
	
	- Red LED: if there's no spot available inside, the red LED will light up, meaning that no one can enter the room.
	
	- Green LED: if there's 1 spot available, the green LED will light up, meaning that another person can use the room. (optional)
	
	- Yellow LED: if there's 0 spot available, the yellow LED will light up.
	
	• Safety: 
	- In environments, like small labs, there may be occupancy limits for safety regulations.
	- This system helps ensure compliance by allowing managers to check and control room capacity.
	
	• Energy efficient:
	- By tracking room usage, the system can be paired with automated lighting, ensuring energy only gets used when people are present, reducing unnecessary consumption.
	
	• Battery:
	- The system will be fully powered using a 9V lithium battery which should last long enough before the next battery change.
 
	• IR proximity sensor:
	- Whenever someone passes through the main room door, the sensor 1 will automatically detect someone's presence and register the count as one person inside.
	- By using two IR sensors placed in sequence, the system detects the direction of movement. 
	- If the first sensor triggers before the second, it records an entry; if the second triggers before the first, it records an exit. 
	- This directional detection minimises errors, providing reliable, correct counts.
 
	• LCD display:
	- A LCD display is used to show how many spaces in realtime are being occupied inside the room.
	- This makes it easy for its users to know how many people are present without needing to enter the room or manually count.
 
	• Buzzer: 
	- When the washroom is full, the buzzer will produce a sound at a certain frequency so that you know it's full and can not enter immediately.
	
	• Cost effective: 
	- As the components are readily available.
	
#### Main components

	• Microcontroller (ATmega328p)
	• Infra red LED
	• Photodiode
	• LCD display (16 x 2)
	• Capacitors
	• Lithium battery (9V)
	• Buzzer
	• LEDs (Red/Green/Yellow/Blue)
	• 16 MHz crystal oscillator
	• Resistors
	• Pull up resistors
	• Push buttons
	• 28-pin IC socket
	• Voltage regulator (LM7805_smd)
	• Inductor
	• Potentiometers
	• 2-pin connector
	• Dual comparator (LM393)
	• Jumpers
	• Switch
	• Bipolar Junction Transistor (BC547C)
	
##### Programming

	• Notepad ++ will be used to write the main.c file.
	• The microcontroller (ATmega328p) will be flashed using myAVRboard MK2.