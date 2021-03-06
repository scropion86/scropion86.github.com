---
published: true
layout: post
description: a small intro into IOT with my own design of PCB
modified: 15/10/2015
tags:
  - IFTTT
  - Blynk
  - IOT

---



# EgyIot ESp8266 PCB IOT board

Hello Blynkers,

as a new maker (5 months ) I just started using Arduino UNO and a breadboard but after that i know the limitation of that specially in connecting it to other thing. after that I start to see ESP8266 blowing everything else with very high potential and ideas. but ESP8266 is not breadboard friendly (before NodeMcu and Wemos D1/D1 mini shows up) and even if you create your own adapter you have to connect to many resistors and pull-up and Pull-down many pins to get the board in boot mode or flashing mode. even after that you will have many jumper wires and even with prototype board and soldering you will either have a big size board or clunky wires.

as I start playing with Arduino and ESP8266 MCU I immediately think why not to use it to switch things on/off and what about control LED lights also so , I started that on breadboard and it's working , but again too much jumpers wires and endless issues because of the moving wires , and to do it in prototype board with a lot of soldering work and time it works fine but not looks like something I can use it in-wall electricity box so I start learning how to transfer my project from breadboard to PCB.

Learning EAGLE CAD for PCB layout and schematics , reading too many Datasheets of parts that I need to use it in my board like MOSFETs , Transistors , Relays etc. That takes me a lot of time and what I like that I learn a lot of things here that I will never know if I didn't go that farther in electronics. I designed the schematic and also Layout in EAGLE but because I live in Saudi Arabia – but I'm Egyptian – and all the parts and PCB has to be imported as I will never find a PCB Manufacturer or a Parts supplier here so any mistake will takes me along time and additional cost to re-manufacture the PCB and source the parts again. So I show my design in www.esp8266.com to get help in my schematic if any mistake or wrong part used and I can't describe how these guys helped me out to get the schematic With almost no error. Here I must thank the martinayotte and AdrianM from www.esp8266.com they helped me a lot to fix some mistakes in my

**PCB size**: 92X55 mm

**MCU** : ESP8266/ESP-12F

**power**:

* Built in power supply AC/DC 5V@0.6A
* 3.3V regulator for ESP-12F
* 12V power input for LED strip

**Relays:** 3 relay 10A (advised to use it up to 3A max).

**LED strip :** 3 channel – RGB – LED strip supported(advised 3A max per channel).

**GPIOs** all the GPIOs is broken to a male header if you want to use it for a different purpose.

**EAGLE CAD layout**

![enter image description here][1]

**PCB after manufactured**

![enter image description here][2]


**the PCB with all parts exibrt ESP-12F**
![enter image description here][4]

**the complete Board with parts**

![enter image description here][3]

**Disclaimer**

I accept no responsibility for any damage caused through following advice in these pages. When dealing with mains voltages.Please take some professional electronic designer before to use any of my designs or advises as I am totally Hobbyist just doing this for Fun.

[1]: http://i.imgur.com/HsqmZqa.png
[2]: http://i.imgur.com/RxTpbJ2.jpg
[3]: http://i.imgur.com/CbHJjro.png
[4]: http://i.imgur.com/FuJos8V.jpg
