# Pick-n-Place-Robot-Arm

## Abstract:

This project involved designing and building a pick and place robot that can autonomously pick up objects and place them at desired locations. The robot utilizes potentiometers to allow granular control of the joint angles and end effector position. An Arduino microcontroller reads the analog voltage values from the rotating potentiometers and controls servo motors to achieve proportional angular motion. The robot was successfully built using basic components like servos, potentiometers, Arduino Uno, and laser-cut acrylic frames. It demonstrates the application of embedded systems and electronic components for developing customizable robotic systems. The potentiometer control scheme provides an intuitive way to control the robot manually. In the future, this project can be enhanced by adding computer vision for autonomous pick and place operation.

## Introduction:

Pick and place robots are used widely in industries and warehouses for repetitive material handling tasks. This project involved designing a smaller scale customizable pick and place robot that can be controlled manually using potentiometers. Potentiometers are variable resistors which produce an analog output voltage proportional to the shaft rotation angle. This analog value can be used to control servo motors for precise angular positioning. 

The aim of this project was to build a basic 2-axis robotic arm with an end effector that can pick up small objects and place them at desired locations as set by the user via potentiometers. The robotic arm was designed with two joints to provide movement in the vertical and horizontal planes. The major components used were Arduino Uno, SG-90 servos, 10k potentiometers, acrylic frames and a gripper.

## Methodology:

The robotic arm was designed with two servo-driven joints for the base and elbow. The base servo rotates the entire arm horizontally while the elbow joint provides vertical motion. The acrylic frames were laser cut to the required arm dimensions and servo horn slots. 

Two 10k potentiometers were integrated into the control box to adjust the base and elbow servo angles. The potentiometers were connected to analog input pins A0 and A1 of the Arduino Uno. As the potentiometer shaft is rotated, the analog voltage divides accordingly. This analog input was mapped to servo angles in the range 0-180 degrees using the Arduino map function. 

The Arduino reads the analog voltage and sets the corresponding servo angle via PWM (pulse width modulation) signal. Continuous rotation of the potentiometers provides proportional control of the joint motion. The end effector was 3D printed with a servo-driven gripper to pick and place objects.

## Results:

The pick and place robot was successfully built and tested for basic object manipulation tasks. The potentiometers provided intuitive control over the joint angles with near 360-degree movement. The gripper was able to pick up small objects up to 50 grams mass and place them precisely at desired locations mapped to potentiometer settings. Some limitations were noticed at extreme joint angles where the base servo experienced torque issues. The arm was also prone to vibration during rapid motion.

Overall, the project achieved accurate manual control of a 2-axis robotic arm via analog potentiometer inputs. It demonstrated the integration of basic electronic components like servos and sensors with an Arduino microcontroller to develop customizable robotic systems. In the future, computer vision and autonomous path planning capabilities can be added to enable picking arbitrary objects from a bin and placing them accurately.

## Conclusion:

This project involved developing a basic 2-axis pick and place robot that can be controlled manually using potentiometers. The major achievements were:

- Designed a 2-DOF robotic arm with servo motors and 3D printed parts

- Integrated Arduino with analog potentiometers for proportional control 

- Mapped potentiometer angles to servo angles to achieve intuitive joint motion

- Programmed Arduino to read analog voltage values and drive servo angles

- Implemented a servo-based gripper to pick and place small objects

The potentiometer control scheme provided granular control over the robot movement and allowed picking and placing objects precisely. In the future, this project can be enhanced by adding more degrees of freedom, sensors and autonomous control capabilities.

## Difficulties Faced and Future Enhancements:

 - Initialization : Use servo.attached() instead of pinMode() to initialize the servos
    
 - Smoothening the motion : Add smooth servo motion using servo.writeMicroseconds()

 - Jitter : Prevent servo jitter by adding small delays between movements

 - Design Enhacements : Use of Acrylic Glass for robot links