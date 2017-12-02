# PRmakerspaceIOTworkshop

IOT Workshop
Dec 2, 2017
1.	What is IOT?
2.	What is NodeMCU?
a.	ESP8266
b.	Why NodeMCU?
c.	Comparison to other boards (Lolin V 3 vs Other Boards)
d.	ESP8266 Projects and Resources (Andres, etc.)
3.	NodeMCU Pin Layout: 
a.	V2 
b.	V3
c.	Note: 
i.	LoLin is the brand purchased, also Amica.  Amica seems more stable at times (the one I bought), but LoLin has a VU pin for 5v output.
ii.	Pins in sketches for Arduino may have different pin names.  Need to convert

4.	Setup NodeMCU
a.	Driver
b.	Preferences -> Board Managers URL -> ESP8266json file	
c.	Board Manager -> Install ESP8266
d.	Board Selection, Port Selection, Baud Rate (importance)
5.	Install Libraries - Required
a.	ESP8266
b.	Adafruit MQTT Library (options)
6.	Install Libraries – Optional
a.	HTTP
b.	Adafruit Unified Sensors
c.	DHT
7.	MQTT
a.	What is MQTT?
b.	MQTT Pub/Sub process
c.	Benefits of MQTT -> navigate routers easily, small packets, etc.
d.	Cons of MQTT -> Learning curve, unconventional, security, setup (rPi), etc.
e.	MQTT vs HTTP vs Websockets-> IFTTT (Webhooks), 
https://systembash.com/mqtt-vs-websockets-vs-http2-the-best-iot-messaging-protocol/
https://iot.stackexchange.com/questions/1492/what-is-the-difference-between-mqtt-and-web-sockets-and-when-should-i-use-them
https://github.com/nassir-malik/IOT-ESP8266-Google-Home
f.	MQTT Brokers -> Adafruit, Thingspeak, Mosquito (rPi), Node Red, etc.

8.	Adafruit.io
a.	MQTT Broker -> Feeds (graph, tables, etc.), Dashboard, Triggers, Limits, Rest API
b.	Setup Account -> Note username and key
9.	Example 1 -> mqtt_esp8266
a.	Adafruit.io -> 2 new feeds -> photocell, onoff
b.	Examples -> Adafruit MQTT Library -> mqtt_esp8266
c.	Setup WiFi Credentials, Adafruit Credentials, discuss using .h files for credentials
d.	Upload and observe serial port -> See subscription process
e.	Adafruit.io -> create dashboard -> create new blocks (on/off button, photocell gauge)
f.	Observe gauge as publish happens, interact with on/off and watch in serial
g.	Discuss Code
10.	Example 2 -> mqtt_2subs_esp8266
a.	Adafruit.io -> 1 new feeds -> slider 
b.	Examples -> Adafruit MQTT Library -> mqtt_2subs_esp8266
c.	Setup WiFi Credentials, Adafruit Credentials
d.	Adafruit.io -> create dashboard -> create new block (slider named slider, 0 - 180)
e.	Upload and observe serial port -> See subscription process
f.	Interact with on/off and watch in onboard LED, interact with slider and watch serial
g.	Note ping process for keeping mqtt connection alive
h.	[Optional] -> Open ESP8266 Servo code and add to this sketch based on slider
11.	Example 3 -> mqtt_esp8266_callback
a.	Examples -> Adafruit MQTT Library -> mqtt_2subs_esp8266
b.	Setup WiFi Credentials, Adafruit Credentials
c.	Set timezone to -8
d.	Upload and observe serial port -> See subscription process
e.	Observe non-RTC time stamp, organizing via callbacks
12.	IFTTT Integration
a.	Setup Account, Connect Adafruit, Send to a gmail address based on values
b.	Gmail email -> scan for keyword -> send subject/body value (ON/OFF)
c.	Webhooks, POST, etc.
13.	Adafruit API
a.	Restful requests
b.	https://www.jeremymorgan.com/internet-of-things/how-to-adafruit-io/
c.	Use Postman to test
d.	https://codepen.io/Quoclon/pen/POxRQG
e.	Rest – PUT: https://www.youtube.com/watch?v=zc1O-GogM6I
f.	
14.	


15.	Troubleshooting
a.	Router issues -> use my phone instead
b.	Upload issues -> driver, baud, unplug, re-flash, https://github.com/kentaylor/EraseEsp8266Flash
c.	5V -> 5 volt should be used on the VU pin 5V output/input via VIN (can use VIN?)

16.	Further Resources
a.	MQTT
i.	https://www.baldengineer.com/mqtt-tutorial.html
ii.	Andres
iii.	Adafruit MQTT Series
b.	Servo Tutorial:
i.	https://mounishkokkula.wordpress.com/servo-motor-tutorial-esp8266-nodemcu/
17.	Interesting Projects:
a.	https://medium.com/@rxseger/esp8266-first-project-home-automation-with-relays-switches-pwm-and-an-adc-ad25f317c74f
18.	Alternative Methods:
a.	HTTP, ESP8266 Webserver, ESP-ESP communication, Mosquito, Raspberry Pi
19.	


Optional Libraries
MultiWifi Github (allow for configuration of ESP8266 to new Wifi)
•	Haven’t been able to setup with my current configuration
•	https://github.com/tzapu/WiFiManager


