# Aquarium Automation using NodeMCU ESP-12E V3.0 🐟

> 📢 **Development Notice**: This ESP8266 version will no longer receive feature updates. A new ESP32 edition is under development that will provide more powerful customization options and advanced monitoring features for aquarium inhabitants. Stay tuned! 🚀

<div align="center">

[![License](https://img.shields.io/github/license/desiFish/Smart-Aquarium-V3.0?color=blue&style=for-the-badge)](https://github.com/desiFish/Smart-Aquarium-V3.0/blob/main/LICENSE)
[![Stars](https://img.shields.io/github/stars/desiFish/Smart-Aquarium-V3.0?style=for-the-badge&color=yellow)](https://github.com/desiFish/Smart-Aquarium-V3.0/stargazers)
[![Issues](https://img.shields.io/github/issues/desiFish/Smart-Aquarium-V3.0?style=for-the-badge&color=green)](https://github.com/desiFish/Smart-Aquarium-V3.0/issues)
[![Arduino](https://img.shields.io/badge/Arduino-IDE-00979D?style=for-the-badge&logo=Arduino&logoColor=white)](https://www.arduino.cc/)
[![ESP8266](https://img.shields.io/badge/ESP8266-IoT-red?style=for-the-badge&logo=esphome&logoColor=white)](https://www.espressif.com/)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-no%20(ESP32%20coming%20soon)-red.svg?style=for-the-badge)](https://github.com/desiFish/Smart-Aquarium-V3.0/graphs/commit-activity)
[![Website](https://img.shields.io/website?style=for-the-badge&up_message=online&url=https%3A%2F%2Fgithub.com%2FdesiFish%2FSmart-Aquarium-V3.0)](https://github.com/desiFish/Smart-Aquarium-V3.0)
[![made-with-arduino](https://img.shields.io/badge/Made%20with-Arduino-1f425f.svg?style=for-the-badge)](https://www.arduino.cc/)

</div>

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

> Important: Do not fetch power from ESP GPIO Pins for relay board. Connect GND between NodeMCU, Relay and power supply.

## 🛠️ Required Components

<div align="center">

### Core Components

<table>
<tr>
    <td align="center">
        <img src="https://robu.in/wp-content/uploads/2021/11/5v-4-channel-ssr-solid-state-relay-module-240v-2a-output-with-resistive-fuse-tech7978-6426-2-550x550-1.jpg" width="200px" alt="Relay Board"/><br />
        <b>Relay Board</b><br />
        <sub>4 Channel 5V SSR</sub><br />
        <sub>250V 2A with Resistive Fuse</sub>
    </td>
    <td align="center">
        <img src="https://m.media-amazon.com/images/I/41RP9FjC+jL.jpg" width="200px" alt="DS3231"/><br />
        <b>RTC Module</b><br />
        <sub>DS3231 I2C</sub><br />
        <sub>Precision RTC</sub>
    </td>
</tr>
<tr>
    <td align="center">
        <img src="https://m.media-amazon.com/images/I/51lIrI5vnQL.jpg" width="200px" alt="NodeMCU"/><br />
        <b>Microcontroller</b><br />
        <sub>NodeMCU-ESP8266</sub><br />
        <sub>ESP12E Development Board</sub>
    </td>
    <td align="center">
        <img src="https://www.electronicscomp.com/image/cache/catalog/13-inch-i2c-iic-oled-display-module-4pin-white-800x800.jpg" width="200px" alt="OLED"/><br />
        <b>OLED Display</b><br />
        <sub>1.3" I2C I2C 128x64</sub><br />
        <sub>Any Color</sub>
    </td>
</tr>
</table>

</div>

## 🌐 Web Interface

<div align="center">

<table>
<tr>
    <td align="center" colspan="2">
        <img src="https://github.com/chikne97/Smart-Aquarium-V3.0/blob/main/demo2.png" width="800px" alt="Web Interface"/><br/>
        <b>Responsive Web Dashboard</b>
    </td>
</tr>
<tr>
    <td align="center" width="50%">
        <h3>🎮 Control Features</h3>
        <ul align="left">
            <li>⏱️ Time-based automation</li>
            <li>🔌 Manual device control</li>
            <li>⚡ Power saver mode</li>
            <li>⏲️ Custom timer settings</li>
        </ul>
    </td>
    <td align="center" width="50%">
        <h3>📊 Dashboard Features</h3>
        <ul align="left">
            <li>📡 Real-time status updates</li>
            <li>📱 Mobile-responsive design</li>
            <li>🔔 Visual status indicators</li>
            <li>📈 Device runtime statistics</li>
        </ul>
    </td>
</tr>
</table>

</div>

## 🤝 Contributing
We welcome contributions! Here's how you can help:
- 🔀 Fork the repository
- 👩‍💻 Create your feature branch
- ✨ Make your changes
- 📝 Open a Pull Request

## 🚀 Future Aspects
Here's what more can be done:
- 📱 Mobile App Integration
- 🌡️ Temperature Control
- 💧 Water Level Monitoring
- 🔄 Auto Water Change System

See our [Issues](https://github.com/desiFish/Smart-Aquarium-V3.0/issues) page for detailed roadmap and planned features.

## 🔄 Future Updates
See [Issues](https://github.com/KamadoTanjiro-beep/Smart-Aquarium-V3.0/issues) for planned features and improvements.

## 📄 License Summary

<details>
<summary>Click to expand detailed license information</summary>

<table>
<tr>
    <th colspan="2">GNU General Public License v3.0 Details</th>
</tr>
<tr>
    <td><b>Permissions</b></td>
    <td>
        ✅ Commercial use - Use for business purposes<br>
        ✅ Modification - Modify the code<br>
        ✅ Distribution - Share the code<br>
        ✅ Patent use - This license provides an express grant of patent rights from contributors
    </td>
</tr>
<tr>
    <td><b>Conditions</b></td>
    <td>
        📝 License and copyright notice - Include the original license and copyright<br>
        📝 State changes - Document all changes made to the code<br>
        📝 Disclose source - Source code must be made available when distributing<br>
        📝 Same license - Modifications must be released under the same license
    </td>
</tr>
<tr>
    <td><b>Limitations</b></td>
    <td>
        ⚠️ No Liability - Author is not responsible for damages<br>
        ⚠️ No Warranty - Code is provided "as is"<br>
        ⚠️ Must preserve copyleft - Cannot change to a more restrictive license
    </td>
</tr>
</table>

<sub>This is a copyleft license that requires anyone who distributes your code or a derivative work to make the source available under the same terms.</sub>
<br>
<sub>For complete license text, see [LICENSE](/LICENSE)</sub>
</details>

---

<div align="center">

### Made with ❤️ for the IoT Community

<p>
<a href="https://github.com/desiFish/Smart-Aquarium-V3.0/stargazers">⭐ Star this project</a> &nbsp;|&nbsp; 
<a href="https://github.com/desiFish/Smart-Aquarium-V3.0/issues">🐛 Report Bug</a> &nbsp;|&nbsp;
<a href="https://github.com/desiFish/Smart-Aquarium-V3.0/issues">✨ Request Feature</a>
</p>

</div>
