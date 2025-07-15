# Esp-sheets-
 a  way for u too use an esp to edit and read  a google sheet
how to use
  get arduino ide
  
  install these dependencies on arduino library manager

  
  #include <ESP8266WiFi.h>
  
  #include <WiFiClientSecure.h>
  
  
  #include <ESP8266HTTPClient.h>
  
  
  #include <ArduinoJson.h>

  use this tutorial to get the dependencies to code a esp8266 using arduino ide
  https://randomnerdtutorials.com/how-to-install-esp8266-board-arduino-ide

   replace these with the required
  const char* ssid = "wifi ssid";
  const char* password = "passowrd";

  open a google sheet and name it whatever u want
  <img width="637" height="441" alt="image" src="https://github.com/user-attachments/assets/6a3e20e3-0087-4794-a6be-5506d7fbfdcc" />

  
  then add the name sof the switches you want to control in a1 ,a2 and a3

  
  <img width="637" height="441" alt="image" src="https://github.com/user-attachments/assets/50d37d23-c800-475d-b61f-2808d5d2d3ed" />
  
  the code edits b1,b2,b3 as 0,1 as on and off

  click extensions and then app scripts 

  <img width="727" height="309" alt="image" src="https://github.com/user-attachments/assets/3d6ab7c9-3ad5-4789-ab3d-731afce1a59f" />

 u will see code.gs put youre desired code here
 we will start by setting up the receiver

 copy receiver pull code.gs here which pulls value of b1 ,b2,b3 simultaneously

 <img width="1920" height="1080" alt="image_2025-07-14_195816005" src="https://github.com/user-attachments/assets/dfa3dc2b-cfa7-4a2a-827d-a02a1e1fcce5" />

 
 <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/3c66cfe5-0cfd-44da-9ff5-d53ffaa8c05a" />

 click deploy , new deployment

 <img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d5bf4ec6-4ff6-4eb9-810b-62449601e970" />

click selct type and choose webapp


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d0a9dade-d106-4642-ba31-606f5a092581" />

name it whatever u please and set access as anyone

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/cdc09459-39b1-4573-91c8-3e1ebad86bc9" />


click deploy

authorize access

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/511e3e1d-5505-4a89-9464-42e2c4308cc9" />


u might get this

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/7bee8d1e-dbf1-432f-9fe4-be045b830429" />

this is common for authorizing google app scripts
click advanced 
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/06d72dc7-99d7-4fef-853a-a5ac7ec0b07c" />

and allow

u will get a web app url this is important
copy this down and replace it here in the arduino code
(make sure to have no spaces before and after)

const char* url = "url";

now connect up your receiver according to this diagram

<img width="1085" height="610" alt="image" src="https://github.com/user-attachments/assets/1e340d2e-948b-430f-868d-a6d236ccb55b" />


 attach a thread to the servo and stick it to the switch 
 make it so tht=t the servo hits the switch when set to 0 and pulls away maximum possible when set to 180 so that it plls the switch and turns on the switch  ( usually when setting a servo to 180 using an arduino it moves 90 degrees from 0 degrees position)

 now for the trans mitter

 noww repeat the same process with the b1.gs code ( just click app scripts and redo the process dont woryy it doersnt delete the code of the receiver it just makes a new code )
 now that u have the url for the transmitter
 replace this in the transmitter.ino code with the url 
 const char* b1= "url";
 repeat for b3.gs
const char* b3 ="url";

and for b2.gs
const char* sr2 = "url";

follow this wiring diagram for the transmitter


**<img width="1042" height="524" alt="image" src="https://github.com/user-attachments/assets/5f4adb59-c19c-4860-8352-6f04101eb648" />
**
 
now u should be done jsut turn both of them on wait 10 seconds for it to connect to the internet
and fire away(fyi the first button press sets the cell to on )
 

