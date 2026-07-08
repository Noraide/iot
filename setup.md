# Setup ESP32 Board
How to deploy a model

## Step 1: Download Arduino IDE
[Arduino IDE ](https://www.arduino.cc/en/software/)

## Step 2: Install ESP32 Board
Go to File > preferences > Additional Boards Manager URLs
copy and paste
```bash
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json, http://arduino.esp8266.com/stable/package_esp8266com_index.json
```
Go to board and search esp32
install esp32 by Espressive Systems

## Step 3: Install Library
Go to library and search Blynk

install Blynk by Blynk

## Step 4: Test ESP32 Board
  1. Connect ESP32 Board
  2. select ESP32 Dev Module and
  3. select port
  4. Go to File > Examples  > WiFi > WiFiScan
  5. Upload the program and check serial monitor for WiFi ssid

## Step 5: Test WiFi Connection
Download wifitest program

[Wifitest](https://github.com/Noraide/iot/blob/main/wifitest.ino)

Edit ssid and password

Upload the program
