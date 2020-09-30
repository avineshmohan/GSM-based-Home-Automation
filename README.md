# GSM-based-Home-Automation
This can hep you to access your home when you are out . You can switch on and off the home appliances from anywhere without any wifi or network connection.


Mobile phone is a revolutionary invention of the century. It was primarily designed for making and receiving calls & text messages, but it has become the whole world after the Smart phone comes into the picture. In this project we are building a home automation system, where one can control the home appliances, using the simple GSM based phone, just by sending SMS through his phone. In this project, no Smart phone is needed, just the old GSM phone will work to switch ON and OFF any
Working Explanation

In this project, Arduino is used for controlling whole the process. Here we have used GSM wireless communication for controlling home appliances. We send some commands like “#A.light on*”, “#A.light off*” and so on for controlling AC home appliances. After receiving given commands by Arduino through GSM, Arduino send signal to relays, to switch ON or OFF the home appliances using a relay driver.

Here we have used a prefix in command string that is “#A.”. This prefix is used to identify that the main command is coming next to it and * at the end of string indicates that message has been ended.

When we send SMS to GSM module by Mobile, then GSM receives that SMS and sends it to Arduino. Now Arduino reads this SMS and extract main command from the received string and stores in a variable. After this, Arduino compare this string with predefined string. If match occurred then Arduino sends signal to relay via relay driver for turning ON and OFF the home appliances. And relative result also prints on 16x2 LCD by using appropriate commands.

Here in this project we have used 3 zero watt bulb for demonstration which indicates Fan, Light and TV.

Below is the list of messages which we send via SMS, to turn On and Off the Fan, Light .

GSM Module:

GSM module is used in many communication devices which are based on GSM (Global System for Mobile Communications) technology. It is used to interact with GSM network using a computer. GSM module only understands AT commands, and can respond accordingly. The most basic command is “AT”, if GSM respond OK then it is working good otherwise it respond with “ERROR”. There are various AT commands like ATA for answer a call, ATD to dial a call, AT+CMGR to read the message, AT+CMGS to send the sms etc. AT commands should be followed by Carriage return i.e. \r (0D in hex), like “AT+CMGS\r”. We can use GSM module using these commands:

ATE0 - For echo off

AT+CNMI=2,2,0,0,0 <ENTER> - Auto opened message Receiving. (No need to open message)

ATD<Mobile Number>; <ENTER> - making a call (ATD+919610126059;\r\n)

AT+CMGF=1 <ENTER> - Selecting Text mode

AT+CMGS=”Mobile Number” <ENTER> - Assigning recipient’s mobile number

>>Now we can write our message

>>After writing message

Ctrl+Z send message command (26 in decimal).

ENTER=0x0d in HEX

The SIM900A is a complete Quad-band GSM/GPRS Module which delivers GSM/GPRS 850/900/1800/1900MHz performance for voice, SMS and Data with low power consumption.
