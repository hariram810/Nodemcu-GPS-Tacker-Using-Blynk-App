# Nodemcu-GPS-Tacker-Using-Blynk-App

![33](https://user-images.githubusercontent.com/118633170/202870604-d3fbd955-82b6-4171-82f0-1daa2773b071.png)

if you have hard-time 3d printing stuff and other materials which i have provided in this project please refer the professionals for the help, JLCPCB is one of the best company from shenzhen china they provide, PCB manufacturing, PCBA and 3D printing services to people in need, they provide good quality products in all sectors


Please use the following link to register an account in JLCPCB

https://jlcpcb.com/RNA



Pcb Manufacturing

2 layers

4 layers

6 layers


PCBA Services

JLCPCB have 350k+ Components In-stock. You don’t have to worry about parts sourcing, this helps you to save time and hassle, also keeps your costs down.

Moreover, you can pre-order parts and hold the inventory at JLCPCB, giving you peace-of-mind that you won't run into any last minute part shortages.


3d printing


SLA -- MJF --SLM -- FDM -- & SLS. easy order and fast shipping makes JLCPCB better companion among other manufactures try out JLCPCB 3D Printing servies

JLCPCB 3D Printing starts at $1 &Get $54 Coupons for new users

![1](https://user-images.githubusercontent.com/118633170/202870561-ddec10e7-98a3-436a-b7e3-6070c559c415.png)
![2](https://user-images.githubusercontent.com/118633170/202870562-d31b8fb3-8a98-41bc-8f0a-dd491242556c.png)

This is a nodemcu GPS Tracker for tracking simple devices from theft and other possible things can be fixed on a vehicle also with good internet facility by a dongle or some sort of network provider

![11](https://user-images.githubusercontent.com/118633170/202870599-c9bf1f51-2906-4fda-a513-c21699b73156.png)
![22](https://user-images.githubusercontent.com/118633170/202870602-1f7356fd-1060-4849-8442-e11e513f6a98.png)


A GPS tracker is a navigation device generally on a vehicle, asset, person, or animal that uses the Global Positioning System (GPS) to determine its movement and geographic position. GPS tracking devices send special satellite signals that are processed by a receiver. Locations are stored in the tracking unit or transmitted to an Internet-connected device using the cellular network or WiFi worldwide. GPS trackers connect to a series of satellites to determine location. The tracker uses a process called trilateration which uses the position of three or more satellites from the Global Navigation Satellite System (GNSS) network and their distance from them to determine latitude, longitude, elevation, and time.

![11](https://user-images.githubusercontent.com/118633170/202870617-a38b4270-a00e-44c4-b9bb-402bda3f32cc.png)
![22](https://user-images.githubusercontent.com/118633170/202870620-7aa505a2-d51b-4652-b845-98255f3ce494.png)
![33](https://user-images.githubusercontent.com/118633170/202870621-167b0a32-92ae-42e1-a066-237ea77bea02.png)


In this project, we will use Quectel L86 GPS Module and interface it with NodeMCU ESP8266 Board. Instead of Quectel L86 GPS Module, you can also use Neo-6M GPS Module or any other similar GPS Module. Using the TinyGPS library, we will determine the latitude, longitude, speed, bearing as well as the location on Map. We will send all these parameters to the Blynk Application and monitor the real-time data along with the map on Blynk Dashboard.

The L86 is an ideal solution for wearable fitness devices due to its ultra-compact design and low power demands. Its Low Power feature enables GPS connectivity at around half the power consumption of normal mode while in static receiving mode. Combined with its precision and high sensitivity, this makes the L86 suitable also for a broad range of IoT applications such as portable devices, automotive, personal tracking, security, and industrial PDAs.

![234](https://user-images.githubusercontent.com/118633170/202870655-165bf90f-d4d7-4228-999e-5947bf7d63f4.jpg)


The L86 has a patch antenna on top measuring 16.0mm × 16.0mm × 6.45mm, with 66 acquisition channels and 22 tracking channels. It acquires and tracks satellites in the shortest time even at the indoor signal level. The module operates at 2.8V~4.3V with a typical power consumption of 20mA and in Standby mode power consumption is around 1.0mA. To learn more about the L86 GPS module, you can check the L86 Datasheet.

![3](https://user-images.githubusercontent.com/118633170/202870566-867e7689-ba19-40b3-b3c5-9a218abf15ef.png)
![4](https://user-images.githubusercontent.com/118633170/202870567-8f79ed3c-8943-4a42-bfa7-38e37305b04c.png)
![5](https://user-images.githubusercontent.com/118633170/202870568-80553649-1a66-4fdf-80a7-c72a48e0d8b5.png)


The Quectel L86/L80 GPS Module has 12 pins as shown in the image below.

The L86 is a tiny SMD-type Module that doesn’t have any male/female header pins for testing. So you can use the male header pin with 2.54 spacing and solder them on the L86 PCB from the bottom.

Once, you solder all the 12 Pins on the L86 Module, the Module becomes breadboard friendly. You can now insert the module on the breadboard easily.

Circuit for GPS Tracker using ESP8266

![dfgfd](https://user-images.githubusercontent.com/118633170/202870657-8da907af-94c8-477c-b793-e1afdceba760.jpg)

Now let us move to the project part & make Real Time GPS Tracker using ESP8266 & Blynk. The connection diagram is fairly simple.

Connect the VCC/GND of the L86 GPS Module to 3.3V/GND of NodeMCU ESP8266. Do not supply more than 3.3V. Similarly, connect the VCC backup (V_BCKP) with VCC or to an external battery. It won’t work if this pin is not powered.

Connect the RX/TX of L86 to the D1/D2 of the NodeMCU. This is for Serial Communication using Software Serial.

You can use a jumper wire to connect directly or use a breadboard to assemble the circuit. Hence the hardware for GPS Tracker using ESP8266 is ready.


What is ESP8266 and how does it work?


ESP8266 is a low-cost WiFi module that belongs to ESP's family which you can use it to control your electronics projects anywhere in the world. It has an in-built microcontroller and a 1MB flash allowing it to connect to a WiFi. The TCP/IP protocol stack allows the module to communicate with WiFi signals. The maximum working voltage of the module is 3.3v so you cant supply 5v as it will fry the module.

Let's take an example of controlling an LED light using ESP8266 by smartphone. The ESP8266 acts as an interpreter between the LED and the smartphone. Since we are using the Blynk app to control the LED further explanations will be based on it.

Then scroll down until you see the heading "auth token."


Auth token is an authentication code that I have said before. It is to create a secure connection from Blynk app to the ESP8266 by the web server and also to identify the device while it is to be communicated.

Now choose any methods under auth tokens to save the auth code. The auth code should be entered in the program code later.


Setting up the Arduino IDE for programming ESP8266
Before programming the ESP8266 in Arduino IDE you have to change the board manager to ESP8266.

![img-20190706-wa0028_gGj7UFmZJw](https://user-images.githubusercontent.com/118633170/202870711-7cff4ca0-6b1e-4c1e-92c2-58ad9fefa742.jpg)
![dfds](https://user-images.githubusercontent.com/118633170/202870723-70aa61a1-35cd-496e-8ba0-70adb232b14c.jpg)


If you haven't made any projects on ESP8266 before, you have to follow these steps on the website (given below link) to install ESP8266 board manager on Arduino IDE.

https://randomnerdtutorials.com/how-to-install-esp8266-board-arduino-ide/

If you had finished installing the board manager or already had installed it then choose the board manager type as "Generic ESP8266 Module."

![asdfgfds](https://user-images.githubusercontent.com/118633170/202870728-d294b71c-d0a6-4363-97e3-c745c4756e43.jpg)


To communicate your ESP8266 with the Blynk app, you have to add a Blynk library to your arduino IDE folder. For that, you need to download the library file from the link below:

https://github.com/blynkkk/blynk-library/releases

Once you have downloaded it, extract the file and copy the folders. Then open your Arduino folder and click on libraries folder. Right click and click on paste button. You have successfully installed the Blynk libraries.

![sdfds](https://user-images.githubusercontent.com/118633170/202870764-be516818-0824-4175-bc5f-537d310788e2.png)

