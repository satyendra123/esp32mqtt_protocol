# esp32mqtt_protocol
i am using mqtt protocol 
Quickly get started with MQTT
1. Purpose
The purpose of this lesson is to quickly understand what MQTT is and how to use it

Teacher Wang insists on the principle of "learning how to use it first, and then studying it when necessary". You should use the mobile phone when you get it, instead of studying how it is made. When you have the need to make one, you can disassemble it and study it.

2. What is MQTT
MQTT is a network communication protocol
Divided into client and server
Each client can receive data (subscribe) and send data (publish)
Each message consists of subject ( topic) + message content ( data)
MQTT general process

1658129293389

for example
If 客户端1you subscribe to ledthe topic information from the server, then when the server receives a message from any client (3/5/6), as long as the subject of the message is led, the server will send the message to客户端1

Similarly, if 客户端1there are other clients (2/4) subscribed to ledthis topic, the server will also send this message 客户端2to客户端4

Popular understanding主题
Everyone should know that there are monthly exams every month when they are in school. For example, now there are manufacturers (clients) providing test papers to schools (servers) (xx monthly test xx times), then the school (server) will have this test paper at this time. If the students in Class 1 (clients) need to do this test paper, they will go to the designated office of the school to pick up the test paper. If at the same time, the students in Class 2/3/4 also need to do this test paper, then they will also go to the school office to pick up the same test paper. At this time, we find that the school has the function of receiving one message and sending multiple identical messages to multiple clients (it can be understood that the school has its own printing machine and can print it by itself). If a student invents a question and feels very good, he shares it with the school, and the school sends the question to the manufacturer (the manufacturer's question bank will be included). From here, we can also see that each client can receive and send data.

The above description xx月考xx次考试is actually the theme. Now everyone should understand it.

3. MQTT server installation
3.1 No need to buy
If you want to study MQTT, you definitely need an MQTT server. I will teach you a very simple method. You can use your own computer as an MQTT server and ESP32 as a client.

Notice:
Many tutorials on the Internet ask you to buy a server. First of all, buying a server costs money. Also, we just started to study and bought a server. Are you sure that this money will not be wasted? ! So we will start by installing MQTT on our own computer. If it is really needed, I will teach you how to buy and use it.
