# Data-Science-for-IOT
Keuzevak 1OP2

**Contents**

In this repository you will find all the information you need to know in order to recreate this project. 

**Project Description**

In this project we will make a small indoor weatherstation where we measure the temperature, airpressure and the amount of light. This information is then sent to ThingSpeak and our own webserver. The latter of the two will allow us to control anything. This is demonstated with the use of two LED's.

**Preview**
![WhatsApp Image 2022-02-01 at 19 53 43](https://user-images.githubusercontent.com/95235350/152036788-92033b19-40cb-4365-ad44-c25f210f6251.jpeg)
![WhatsApp Image 2022-02-01 at 19 53 44](https://user-images.githubusercontent.com/95235350/152036804-d100b05e-a1a8-4d49-83f2-75a7b2fa6971.jpeg)
![image](https://user-images.githubusercontent.com/95235350/152036905-77c40828-e635-4c19-9363-ffda98af61ce.png)
![image](https://user-images.githubusercontent.com/95235350/152039556-2c573dc4-e853-4318-b941-a93b44f42a4d.png)
Watch this video to see the possibilities of this project: 


**Materials used**

- ESP32s (+ cable to connect ESP to a computer)
- Breadboard
- Jumpercables
- 1x LDR
- 1x BMP280 Temperature and airpressure sensor
- 2 LED's
- 1x 10k Ohm resistor

**Connecting the Components**

Place the ESP32s on the breadboard. I am using the NodeMCU32s, but any ESP32 will work. Connect the 3.3V of the ESP32 to the + rails on the side of the breadboard. Same goes for the ground of the ESP32. Place the BMP280 on the breadboard and connect it as following:
VCC - 3.3V
GND - GND
SCL - GPIO22
SDA - GPIO21
CSB - Do not connect to anything
SDO - GND

Next we will connect the LDR. Stick one end of the LDR in the 3.3V and one somewhere on the breadboard. Connect this second end with a 10k Ohm resistor to GND and also to GPIO13. See the image below for clarification. Finally we connect two LED's to the ESP. I used GPIO26 and GPIO27 for this. Since the ESP outputs 3.3V there is no need for a resistor. Remember to connect the long leg of a LED to the +, in our case the GPIO pins of the ESP32.

![Schematic_DIoT_2022-02-01](https://user-images.githubusercontent.com/95235350/152038967-890b3ef4-d3da-487f-9e03-53823ab21dfd.png)

**Program the ESP**

Connect the ESP to a computer and upload the code found in this repository. Please replace the network credentials with your own. Also replace the channelID and write APIkey of ThingSpeak with your own. Upload the code while pressing down the boot button on the ESP. Once the code is uploaded press the EN button to reset the ESP. To see the IP-address of your ESP, open the serial monitor. To access the webpage of the ESP, type this IP-address in your browser and press enter. You have to be on the same network as the ESP for this to work.

And that it! You just build your own litte weatherstation with its own webserver which you can use to control anything you want.

**IoT Pipeline**
![Untitled Diagram drawio](https://user-images.githubusercontent.com/95235350/152040351-88dc798c-a972-47d0-ae28-4023a0414bb3.png)

ChannelID ThingSpeak used: 1635214
