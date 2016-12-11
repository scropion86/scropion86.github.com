---
published: true
layout: post
description: Demo post displaying the various ways of highlighting code in Markdown.
modified: 15/10/2015
tags:
  - IFTTT
  - Blynk
  - IOT
[//]:   # we use this also for comments
[//]:   #image:
[//]:   #  feature: header1.jpg

---
# Blynk + IFTTT configuration

![enter image description here][1]

**Hi**

**as the great Blynk team is working on many new features and widgets , and they already promise to provide the push button trigger "as set an icon on your home screen to activate an GPIO on your board" but i think this maybe will take them some time, so tried to use [IFTTT][2] to be integrated with Blynk.**

also you can use IFTTT to do some Automation based on other service -IFTTT call it channels – you have and that will actuate and change the values of your hardware running Blynk .

* * *

examples will be demonstrated.

1. that can be used for many thing but here i will go for the basic tasks like click the icon to make your `D4` GPIO high and that will actuate a relay that will switch on your fan or light.
2. when your Mobile connect to your home WIFI the entrance light will switch on – assuming you have a MCU board connected to Blynk and has a relay that's connected to your entrance lights.
3. please post your ideas in the comments.

that can be used for many thing but here i will go for the basic tasks like click the icon to make your `D4` GPIO high and that will actuate a relay that will switch on your fan or light

* * *

## Requirement:

1. any exist board that already have Blynk sketch running on it.
2. [IFTTT][2] account
3. DO Button by IFTTT app installed [IOS][3] and [Android][4]
4. Mobile phone with IFTTT app installed [IOS][5] or [Android][6]. that's all

—

**here we will try the DO Button**

* open your Blynk dashboard that will be connected to IFTTT and write down the token also you need to Know which GPIO or PIN you need to control eather it's actuall PIN or Virtual.

> Please note that token is has to be kept private as any body have your token can control your Hardware.

* Open DO App in your phone.
* Click on the `+` bar in the top middle.

![enter image description here][7]

* type in the search bar `Maker`.

![enter image description here][8]

* select the Maker channel and connect it.
* from Maker channel select `make a Web Request`. –![enter image description here][9]
* Type Recipe Title like `turn Fan ON` ![enter image description here][10]
* In URL enter `http://blynk-cloud.com//XXXX your TOKEN XXXX/pin/ZZZ`
* and replace `XXXX your TOKEN XXXX` with your actual token and `ZZZ` with the PIN number , for Digital PIN use DX like D1, D5 etc. and for Virtual PIN use VX like V1 ,V5 etc.

> note that if you are using any variant of ESP8266 the pin number here should match the actual GPIO number not as per the board manufacturer numbering .

* in Method select `PUT` to WRITE a value to that PIN.
* in Content Type select `application-json`.
* in body write [`"1"]` to make the PIN High or [`"0"]` to set the PIN Low.
* then click Add button.
* Now for android go to your home screen and try to add widget and search for DO Button and drag it to the selected place and then select the desire recipe name that you Just configured. ![enter image description here][11]
* test it and enjoy.
* * *

**Action based on other IFTTT channels.** **connect to a specific WIFI SSID will change a PIN level to High or Low **
* open IFTTT App in you Mobile.
* click on the top right icon.

![enter image description here][12]

* and click on the `+` icon on the Top right.
* ![enter image description here][13]
* Search on for `Android device` , and select it .

![enter image description here][14]

* scroll down to `Connect to a specific WiFi network` and click on it.

![enter image description here][15]

* Enter the WiFi Network Name that will trigger your Blynk GPIO High or Low.

![enter image description here][16]

* after that click on the second red `+` icon.

![enter image description here][17]

–![enter image description here][18]

* select `Make a Web Request`.

–![enter image description here][9]

* In URL enter `http://blynk-cloud.com/XXXX your TOKEN XXXX/pin/ZZZ`

![enter image description here][19]

* and replace `XXXX your TOKEN XXXX` with your actual token and `ZZZ` with the PIN number , for Digital PIN use DX like D1, D5 etc. and for Virtual PIN use VX like V1 ,V5 etc.

> note that if you are using any variant of ESP8266 the pin number here should match the actual GPIO number not as per the board manufacturer numbering .

* in Method select `PUT` to WRITE a value to that PIN.
* in Content Type select `application-json`.
* in body write [`"1"]` to make the PIN High or [`"0"]` to set the PIN Low.
* then click continue , after that click on finish button.
* * *

enjoy Blynking and please leave any notes , comments , new ideas others can do using the great **Blynk** and IFTTT

[1]: http://i.imgur.com/8gRM6UQ.png
[2]: https://ifttt.com/
[3]: https://itunes.apple.com/us/app/do-button-by-ifttt/id905998610?mt=8
[4]: https://play.google.com/store/apps/details?id=com.ifttt.dobutton
[5]: https://itunes.apple.com/us/app/if-by-ifttt/id660944635?mt=8
[6]: https://play.google.com/store/apps/details?id=com.ifttt.ifttt
[7]: http://i.imgur.com/NZAJ6jh.png
[8]: http://i.imgur.com/qXhzHn8.png
[9]: http://i.imgur.com/a6uv1Hs.png
[10]: http://i.imgur.com/f9OmYqF.png
[11]: http://i.imgur.com/EP8MFFx.png
[12]: http://i.imgur.com/AZzMisE.png
[13]: http://i.imgur.com/SGaGWcm.png
[14]: http://i.imgur.com/TB4jTKD.png
[15]: http://i.imgur.com/hf30vMa.png
[16]: http://i.imgur.com/lZcUpNy.png
[17]: http://i.imgur.com/Bbf1XYE.png
[18]: http://i.imgur.com/8LfbyCc.png
[19]: http://i.imgur.com/c05FpjI.png
