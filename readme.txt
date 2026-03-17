Installation & Setup
1. Environment Preparation
Install Arduino IDE: Download and install arduino-1.8.19-windows.
Driver Installation: Install the CP210x Universal Windows Driver. This is required for your computer to recognize the NodeMCU via USB.

2. Board Configuration
Open Arduino IDE and go to File > Preferences.
In the Additional Boards Manager URLs field, paste the following URL:
http://arduino.esp8266.com/stable/package_esp8266com_index.json

Go to Tools > Board > Boards Manager...

Search for esp8266 and install the esp8266 board manager to enable NodeMCU support.

3. Hardware Connection
VCC -> 3.3V
GND -> GND
SCL -> D1 (on NodeMCU)
SDA -> D2 (on NodeMCU)

4. Uploading the Code
Connect your NodeMCU to your PC using a Micro-USB cable.
Go to Tools > Board and select NodeMCU 1.0 (ESP-12E Module).
Select the correct Port in the Tools menu.
Click the Upload button.
Open the Serial Monitor and set the baud rate to 115200 to see the scan data.

ESP8266 WiFi Strength Meter
A portable WiFi network scanner that detects surrounding wireless signals and displays their SSID and RSSI (Received Signal Strength Indicator) on an I2C OLED display. This project is built using the ESP8266 framework and the Adafruit GFX library suite.

FeaturesReal-time Scanning: 
Automatically refreshes every 5 seconds to find new networks.
OLED Integration: Visualizes network data on a 128x64 SSD1306 display.
Signal Analysis: Displays RSSI values (e.g., -50 is excellent, -90 is poor).
Smart Truncation:Automatically shortens long SSIDs to fit neatly on the screen.
Dual Monitoring: Outputs detailed data to both the OLED screen and the Serial Monitor (115200 baud).

Hardware Requirements

Component    Specification  
Microcontroller    ESP8266 (NodeMCU or Wemos D1 Mini)
Display0.96" OLED (SSD1306) I2C
Connection   I2C (SDA/SCL)
Power  Micro-USB or 3.3V Battery

Libraries Used

To run this code, you must install the following libraries in your Arduino IDE:
ESP8266WiFi: Built-in for ESP8266 boards.
Adafruit_SSD1306: For controlling the OLED hardware.
Adafruit_GFX: For drawing text and graphics

Developed By
Damith Lasdanthha Powered by C-Clarke Institute students
