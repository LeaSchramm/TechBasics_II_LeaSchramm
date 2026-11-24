Types of Movement :

Servo Motors:
-	Anatomy: Inside a micro servo (like the SG90) sits a DC motor, a gear train, a potentiometer, a control unit, and an attached servo horn. 

 Positional vs. Continuous Servos: 
-	Positional servos (such as the SG90) move across a 0–180° angle based on position signals, whereas continuous servos rotate 360° with control based on speed. 
Other Positional Models: 
-	Slides also highlight common positional options like the MG90S micro servo and the TowerPro SG-5010 double ball bearing servo. 
 Basic Servo Control (Exercise 1): 
-	Uses the Arduino Servo.h library (myservo.attach(9) and myservo.write(...) with delay()) to sweep between 0 and 180 degrees, with follow-up challenges to slow down movement and make one direction faster than the return. 
 Potentiometer Control (Exercise 2): 
-	Pairs a servo with a potentiometer using analogRead() and map() to translate analog knob input into servo angles. 
Creative Applications: 
-	Servos are used in robotic arms/hands, animatronic dual eyes, a soft wire-driven oscillating tail, and even a wearable bracelet ("Itch" by Nilufer Musaeva) pairing a micro servo with an ATTiny. 
Joystick Mechanics & Reading (Exercise 3): 
-	A joystick module provides analog readings for X- and Y-axes (wired to A0 and A1) plus a digital pushbutton (wired to pin 2), requiring INPUT_PULLUP and monitored via the Serial monitor. 
Dual-Servo Joystick Setup (Exercise 4): 
-	Mounts a second servo onto the first so one handles X and the other handles Y, letting the joystick steer both axes and pressing the button return them to center. 
<img width="470" height="666" alt="image" src="https://github.com/user-attachments/assets/45e3b278-8150-4da1-a47e-98a803a08a17" />
