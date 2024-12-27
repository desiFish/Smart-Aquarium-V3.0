# Aquarium Automation using NodeMCU ESP-12E V3.0

## ⚠️ Disclaimer
**HIGH VOLTAGE electricity involved!** Use at your own risk. Work under proper supervision if you are a minor. I take no responsibility for any accidents that may occur from using this code.

## 🎯 Features
- Modern responsive web interface
- Asynchronous webserver for better performance
- Real-time page updates using JavaScript XMLHttpRequest
- ESP-NOW time broadcasting to other ESP devices
- Multiple control modes:
  - Automatic (time-based)
  - Power Saver
  - Timer
  - Manual
- Intuitive status display on web interface
- Solid State Relay support for reliability
- Over-the-Air (OTA) updates
- Automatic time synchronization
- Visual feedback and WiFi signal indicators

## 📦 Prerequisites

### Required Libraries
1. [DS3231](https://github.com/NorthernWidget/DS3231) - RTC module
2. [NTPClient](https://github.com/arduino-libraries/NTPClient) - Network time
3. Other libraries available via Arduino IDE Library Manager:
   - ESP8266WiFi
   - ESPAsyncTCP
   - ESPAsyncWebServer
   - Adafruit_GFX
   - Adafruit_SSD1306

### ESP8266 Board Support
Add this URL in Arduino IDE:
```
http://arduino.esp8266.com/stable/package_esp8266com_index.json
```
File → Preferences → Additional Boards Manager URLs

## 🔧 Hardware Setup

### I2C Devices (DS3231 & OLED 128x64)
| NodeMCU | Device |
|---------|--------|
| D1 | SCL |
| D2 | SDA |
| 3.3V | VCC |
| GND | GND |

> Note: Both I2C devices share the same pins. For I2C address conflicts, adjust pull-up resistor values.

### 4-Channel Relay Board
| NodeMCU | Relay |
|---------|-------|
| D3 | IN1 |
| D5 | IN2 |
| D6 | IN3 |
| D7 | IN4 |

> Important: Use separate power supply for relay board. Connect GND between NodeMCU and power supply.

## 🛠️ Required Components

### Core Components
1. **Relay Board**
   - 4 Channel 5V SSR (Solid State Relay)
   - 250V 2A with Resistive Fuse
   - ![Relay Board](https://robu.in/wp-content/uploads/2021/11/5v-4-channel-ssr-solid-state-relay-module-240v-2a-output-with-resistive-fuse-tech7978-6426-2-550x550-1.jpg)

2. **RTC Module**
   - DS3231 AT24C32 IIC Precision RTC
   - ![DS3231](https://m.media-amazon.com/images/I/41RP9FjC+jL.jpg)

3. **Microcontroller**
   - NodeMCU-ESP8266 Development Board ESP12E
   - ![NodeMCU](https://m.media-amazon.com/images/I/51lIrI5vnQL.jpg)

4. **Display**
   - 1.3" I2C IIC 128x64 OLED Display Module
   - White color
   - ![OLED](https://www.electronicscomp.com/image/cache/catalog/13-inch-i2c-iic-oled-display-module-4pin-white-800x800.jpg)

### Additional Requirements
- Appropriate power supplies
- Electrical switches (recommended in series with relays)
- Connecting wires
- Project enclosure

## 🌐 Web Interface
![Web Interface](https://github.com/chikne97/Smart-Aquarium-V3.0/blob/main/demo2.png)

## 🔄 Future Updates
See [Issues](https://github.com/KamadoTanjiro-beep/Smart-Aquarium-V3.0/issues) for planned features and improvements.

## 🤝 Contributing
If you've made improvements to the code, please share them! Contact me with your updates.
