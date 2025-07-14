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




 

