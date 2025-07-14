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


