# ESP32 Smart Home Automation System

**Created by: ArunArudra**

If you use this project, please give proper credit to **ArunArudra**.
This project required significant architecture design, firmware engineering, and system integration work.

---

# 📌 Project Overview

This is a **production-grade ESP32 Smart Home automation system** with:

* ESP RainMaker integration
* MQTT real-time control
* Local Web Portal
* Telegram Bot control
* Remote logging
* Pairing system with secure device linking
* Factory reset and unlink support
* Multi-relay and fan control
* Long uptime architecture (designed for continuous operation)

This system allows users to control devices from:

✔ Physical switches
✔ ESP RainMaker app
✔ Local web portal
✔ Telegram bot
✔ Backend automation

---

# 🧩 System Architecture

```
ESP32 Device
   │
WiFi Network
   │
MQTT Broker
   │
Backend Brain Server
   │
Telegram Bot
   │
User
```

Local Control:

```
User Browser → ESP32 Web Portal
```

Cloud Smart Home:

```
ESP RainMaker → Google Home / Alexa
```

---

# 🛠 Hardware Requirements

* ESP32 development board
* Relay module (2–8 channels supported)
* Optional fan speed control relays
* Push buttons / switches
* Stable WiFi network

---

# 💻 Software Requirements

Install:

* Arduino IDE
* ESP32 Board Package
* ESP RainMaker libraries
* Required Arduino libraries:

```
WiFi
RMaker
WiFiProv
Preferences
AceButton
WebServer
PubSubClient
ArduinoJson
```

---

# ⚙️ Arduino IDE Settings (IMPORTANT)

Board: ESP32 Dev Module
Flash Mode: QIO
Upload Speed: 921600
Partition Scheme: **RainMaker Only**

This project is designed specifically for RainMaker partition.

---

# 🔥 Flashing Firmware

1. Open Arduino IDE
2. Load the firmware file
3. Select correct COM port
4. Verify code
5. Click Upload
6. Wait for completion

After upload → open Serial Monitor (115200 baud)

---

# 📶 First Time WiFi Provisioning

When device boots for first time:

1. Install **ESP RainMaker mobile app**
2. Tap Add Device
3. Scan QR code shown in serial or device label
4. Enter WiFi credentials
5. Device connects to internet

---

# 🌐 Access Local Device Portal

After WiFi connected:

1. Check Serial Monitor for IP address
2. Or check router device list
3. Open browser

```
http://DEVICE_IP
```

---

# 🔐 Portal Login

Default login:

Username: admin
Password: admin

After login you can:

✔ Start pairing mode
✔ Rename device
✔ Unlink device
✔ Factory reset
✔ View pairing code

---

# 🔗 Pair Device with Telegram Bot

### Step 1 — Start Pairing

In portal click:

```
Start Pairing Mode
```

A 6 digit code will appear.

---

### Step 2 — Open Telegram

Search bot name:

```
@YourSmartHomeBot
```

Start bot and send:

```
/connect 123456
```

Replace with your pairing code.

---

### Step 3 — Device Linked

Device becomes paired.
Portal shows paired status.
Telegram control panel becomes active.

---

# 🎛 Telegram Device Control

From Telegram you can:

✔ Turn switches ON/OFF
✔ Control fan
✔ View device status
✔ Rename device
✔ Unlink device
✔ Factory reset

---

# ✏ Rename Device

### From Portal

1. Login portal
2. Enter new name
3. Click update

### From Telegram

Use rename option inside device settings.

Device name updates across system.

---

# 🔌 Unlink Device

### From Portal

Click Unlink Device

### From Telegram

Use Remove Device option

This disconnects user from device.

---

# 🧨 Factory Reset

### From Portal

Enter admin password and confirm.

### From Telegram

Use factory reset command.

### Physical Reset Button

Hold reset GPIO:

3 sec → WiFi reset
10 sec → Factory reset

---

# 🪵 Logs and Events

System records:

* Switch actions
* Remote commands
* Pairing events
* Reset events
* Unlink events

Logs are sent to backend and Telegram.

---

# 🧠 Supported Device Configurations

You can configure:

✔ 2 relay switches
✔ 4 relay switches
✔ 8 relay switches
✔ Fan with speed control
✔ Fan without speed control
✔ Mixed configuration

System supports dynamic device mapping.

---

# 🧯 Troubleshooting

### Cannot access portal

Check IP address or WiFi connection.

### Cannot pair

Ensure pairing mode active.

### Telegram not responding

Check backend server and MQTT.

### Device not showing in RainMaker

Re-provision WiFi.

---

# 🧾 Important Notes

This firmware is designed for long uptime and memory stability.

Do NOT:

* Change partition scheme
* Run multiple MQTT brokers
* Modify RainMaker memory config

---

# ❤️ Credits

Project designed and developed by:

**ArunArudra**

Architecture
Firmware
Backend logic
Integration design

---

# 📜 License and Usage

You are free to use and modify this project for:

✔ Personal use
✔ Commercial projects
✔ Learning
✔ Research

But you MUST:

✔ Give proper credit to ArunArudra
✔ Mention original author in documentation
✔ Not claim original ownership

---

# 🙏 Credit Requirement

If you use this project, include:

```
Powered by ArunArudra Smart Home System
```

or

```
Based on architecture by ArunArudra
```

---

# 🚀 Future Expansion

System ready for:

* WhatsApp integration
* Mobile app UI
* Voice assistant automation
* OTA firmware updates
* Multi-user control
* Device groups and scenes

---

# ⭐ Support the Creator

If this project helped you:

Please give credit to **ArunArudra**.

Your support helps future development.

---

END OF DOCUMENT
