# Object-detection using opencv

# Objective

In this project, we aim to create an Arduino-based wearable device – Third eye for the blind. The “Third Eye for Blind”, is designed to help the blind to overcome the lack of visual sense, by using other senses like sound and touch. It uses audio and vibration signals to notify the user about upcoming hurdle.
There are no such devices available in the market that can be worn like a cloth and having such a low cost and simplicity. When used on a large scale, with improvements in the prototype, it will drastically benefit the community.

# About the Project

Eyes form one of the integral parts of our body, so blindness is such a malady to the persons who are suffering from it. There are several instruments and smart technologies available today for visually impaired individuals to use for navigation, but most of them have significant limitations in terms of portability, and the majority of them require extensive training to use. The goal of this work, Third Eye for the Blind, is to design an object that will be especially useful to those who are physically disabled and regularly rely on others. The third eye for Blind task is a breakthrough that allows outwardly disabled people to move around and between different areas with speed and certainty by detecting nearby obstacles with the help of a worn band that emits ultrasonic waves that alert them with a buzz sound or vibrations. It permits the client the individuals who are outwardly impeded to walk unreservedly by distinguishing the snags. They just need to wear this gadget as a band or fabric on their body.
In this gadget, the distance of the snag is dictated by utilizing an Ultrasonic module and a Microcontroller. The snag distance is estimated and educated to the outwardly impeded individual as a ringer and vibrations. The individual can move in other bearings and stay away from crashes utilizing this. The end consequences of the work would be gloves with a wearable band joined to the gloves to which every one of the segments is associated on a PCB, which works with serious level of precision and unwavering quality.

# Components required

• Arduino UNO
• ESP 32 cam module
• HC-SR04 Ultrasonic sensor
• Vibrating Motor
• Buzzer
• LED RGB
• Connecting wires
• Jumper wires
• Breadboard/Perf board

# Working

![working](https://user-images.githubusercontent.com/77969198/175667053-7d0a8bf3-f1fa-484d-987c-d85c2780e679.png)

Arduino UNO is being programmed with ESP-32 Cam module (programmed using python OpenCV), HC-SR04 ultrasonic sensor, vibrating motor, RGB LED, and buzzer. At the end, after all the connections are done to the Arduino board upload the code to Arduino board and power the other modules using a power bank or the power supply. The Ultrasonic sensor here used as a transceiver. The ultrasonic waves are emitted by the transmitter when the objects are detected. Both the transmitter and receiver re resent inside the ultrasonic sensor.

When the ultrasonic sensor detects the wave impulses from the obstacle near it, the cam module will scan the image and capture it in frames and it will give out the output in form of sound (in the form of speech on obstacle/object recognition), vibration (through vibrating motor) and light (LED RGB). As the blind man is in the proximity of the obstacle, the RGB LED will change from green (safer distance) to blue and when the obstacle is to the nearest, the RGB LED will turn red. The same goes for the buzzer and vibrating motor which will increase the intensity as the object comes closer to the man.

A. Module 1- Arduino UNO

B. Module 2-Buzzer Mode
When the obstacle comes in front of the device it will produce a beep sound and if the way is clear then no sound will be produced.

C. Module 3- Vibration mode
Vibration along with the beep sound will be felt by the device wearer whenever the obstacle is nearer which will help to navigate in a better way.

D. Module 4- ultrasonic sensor
The Ultrasonic sensor is interfaced accordingly. The Ultrasonic sensor pin VCC is connected to the Arduino pin VCC, the Ultrasonic sensor pin GND is connected to the Arduino pin GND, Ultrasonic sensor pin Trig is attached to the Arduino pin 12, Ultrasonic sensor pin Echo is connected to the Arduino PIN 12. The switch used here is for selecting the mode. (Buzzer or vibration mode.)

E. Module 5- RGB led
The RGB LED will change from green (safer distance) to blue and when the obstacle is to the nearest, the RGB LED will turn red.

# Software Implementation

![tinkercad](https://user-images.githubusercontent.com/77969198/175667100-71fed583-abe6-4894-a07d-0d152c2201da.png)

Link for Tinkercad Simulation:

https://www.tinkercad.com/things/0RYi3WyU3Gi-copy-of-ultrasonic-sensor-with-rgb-2/editel?sharecode=HzsCMdp43oRKJ7j1CZskVqlnSpl86troYn2ihZs95MA

OpenCV is then used for object detection and localization through a small camera fitted in the ESP-32 Cam module system. And the text-to-speech library will convert the output to speech which the blind can hear. The class id will be first detected and its reference class name, this will feed the input to the text-to-speech module of python which converts it into audio.

# Results and Discussion

Snaps of object detection
![snap1](https://user-images.githubusercontent.com/77969198/175667141-7634105d-b4a4-4e5b-84d6-fb985a5ea8c3.png)

![snap2](https://user-images.githubusercontent.com/77969198/175667176-a6697d47-2712-46b5-b840-03157bfe7c88.png)

Hardware circuit demonstration
![circuit](https://user-images.githubusercontent.com/77969198/175666162-b4dd3cb9-cd85-4472-ab5f-cfe98e477990.jpeg)

![circuit2](https://user-images.githubusercontent.com/77969198/175666289-595a002e-60ce-4c4a-8748-4b79b5d793ea.jpeg)


# Drive link for working demonstration

https://drive.google.com/drive/folders/1glxZaLZ4dd54n-nVrS-1DmfNCz7_vgPH?usp=sharing

# Conclusion

As a result, this project offered the design and architecture of a new Arduino-based Virtual Eye concept for the blind that can detect objects and obstacles in front of users and warning back signals in the form of voice message and vibrations. To provide constructive assistance and support for the blind and visually impaired, a simple, cheap, efficient, easy to carry, adaptable, easy to handle electronic guiding system with many more astonishing qualities and advantages is proposed. The system will be effective and one-of-a-kind in its capacity to specify the source and distance of things that may come into contact with the blind. It can scan for and recognize obstructions. If the planned architecture is built correctly, the blind will be able to move from one location to another without the assistance of others.

<!-- This allows the blind to know what obstacle is present infront of them. The object detection is done using opencv python and C++ for the blind to know what obstacle is present through the ESP-32 Cam module coded with Arduino Uno accordingly for the desired requirement. The ESP-32 captures pictures through its cam module and detects the recognized object through the captured frames respectively.Also,a text-to-speech converter code is integrated using a python code and required libraries which voices over the object which is detected through the camera. And thus the voice message is generated accordingly.
  -->
