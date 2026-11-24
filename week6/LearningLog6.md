I wasn't able to attend the session but here are my learings from the PPT and YT videos:
Types of Movement 2nd session:

Stepper Motors: 
-	Great for very precise position control and large torque at low speed
-	though trickier to use because they require a matching driver
-	 different motors have different specs and code. 
- How Stepper Motors Work Internally, components include an output shaft, rotor, top coil, bottom coil, and stator

Exercise:

Power Options (Exercise 1): 
-	You can power from an external power module (ensuring a shared ground) or 5V directly from Arduino, though powering a stepper directly from Arduino generally isn't recommended beyond a certain degree.
  
Steps, RPM & moveDegrees(): 
-	Stepper motors move in discrete steps, with steps per revolution varying by motor and driver settings (e.g., stepsPerRevolution may need to be set to 4096 if using your own kit). 
-	RPM helps calculate movement duration, and moveDegrees() converts between steps and degrees. Challenges include testing different moveDegrees() values and making the stepper tick like a clock second-hand. 

move() vs. moveTo() (Exercise 2): 
-	move(clockwise, numSteps) sets relative movement, while moveTo(clockwise, toStep) sets a destination. 
-	A stepper motor doesn't know its current position on its own, with a challenge to alternate clockwise and counterclockwise directions each loop. 

Blocking vs. Non-blocking Functions: 
-	Functions like moveDegrees(), move(), and moveTo() pause/block the Arduino sketch. Use non-blocking equivalents like newMoveDegrees(), newMove(), and newMoveTo() to control other components while moving. 
Touch Sensor + LEDs (Exercise 3): 
-	A touch sensor connects VCC to 5V, GND to GND, and SIG to a digital pin (pin 2, using INPUT: 0 for no touch, 1 for touch) and can stop the motor via stepper.stop(). Adding red and green LEDs (with 220-ohm resistors) signals counterclockwise vs. clockwise movement, with both off when touched. A challenge asks how to remember prior movement and resume after releasing touch. 

Examples & Linear Motion: 
-	Shown in examples like a 3D printer (Prusa MK4S) and eye-like mechanisms, alongside mechanical conversion via a threaded rod vs. pulley + belt. 

Homing a Stepper: 
-	Methods include using a stepper with an encoder, a limit switch (most common), or a contactless magnet + hall effect sensor. 
<img width="470" height="638" alt="image" src="https://github.com/user-attachments/assets/b3a72a00-a06e-4f38-adb3-495d6c59559c" />
