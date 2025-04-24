# Deauth-Guardian
## 🛡 Wi-Fi Deauth Attack Detector using ESP8266

A compact and efficient device to *detect Wi-Fi deauthentication (deauth) attacks* in real-time using an *ESP8266, **buzzer, and **NeoPixel LED*. Designed to be a portable security tool to alert users of potential network threats by detecting suspicious Wi-Fi activity like deauth packets commonly used in denial-of-service or man-in-the-middle attacks.

---

## 📸 Project Overview

This device monitors Wi-Fi traffic and detects deauthentication packets. Once such a packet is detected, it immediately *alerts the user* using:

- 🔊 A *buzzer* for audible alerts  
- 🌈 A *NeoPixel LED* that turns *red* during attack (green by default)  
- ⚡ Powered by an *ESP8266 (NodeMCU / Wemos D1 Mini)*

> Ideal for cybersecurity enthusiasts, penetration testers, and network admins.

---

## 🧰 Features

✅ Detects deauthentication packets (a common type of Wi-Fi DoS attack)  
✅ Visual and audible alert system (NeoPixel + Buzzer)  
✅ Low power, compact, and portable  
✅ Easy to build and open source  
✅ Plug & play – no configuration needed after uploading the code  

---

## 🖥 Hardware Required

| Component           | Description                      |
|--------------------|----------------------------------|
| ESP8266            | Wemos D1 Mini or NodeMCU         |
| Buzzer             | Passive or active buzzer          |
| NeoPixel LED       | WS2812 RGB LED (Single or Ring)  |
| Jumper Wires       | Male-to-Female recommended       |
| USB Cable          | For power & programming          |
| Breadboard (opt.)  | For prototyping                  |

---

## 🔌 Circuit Connections

| Component   | ESP8266 Pin |
|-------------|-------------|
| Buzzer      | D1 (GPIO5)  |
| NeoPixel    | D2 (GPIO4)  |
| VCC         | 3.3V        |
| GND         | GND         |

> Make sure to power the NeoPixel LED with a proper capacitor and resistor (optional but recommended for stability).

---

## 📲 Installation

1. *Install Arduino IDE*  
   [Download here](https://www.arduino.cc/en/software)

2. *Add ESP8266 Board Manager URL*  
   Open Arduino IDE → File → Preferences →  
   Add: http://arduino.esp8266.com/stable/package_esp8266com_index.json

3. *Install Required Libraries*  
   - Adafruit NeoPixel  
   - ESP8266WiFi  
   - ESP8266WiFiScan (or custom Wi-Fi packet sniffing library)

4. *Upload the Code*  
   Select your ESP8266 board and COM port → Upload

---

## 🚨 How It Works

- The ESP8266 is set to promiscuous mode to monitor all Wi-Fi packets nearby.
- It filters out *deauthentication frames* (Type: Management, Subtype: Deauth).
- On detection:
  - Buzzer *beeps*
  - NeoPixel LED turns *red*
- When no attack is present:
  - NeoPixel stays *green*

---

## 🧠 Use Cases

- Monitor Wi-Fi security at home or office
- Use as part of penetration testing kit
- Educational project to understand network attacks

---

## 📦 Future Improvements

- OLED display to show SSID and number of deauth packets
- Data logging to SD card
- Battery-powered version with power-saving features
- Notification to phone via ESP-NOW or MQTT

---

## 🔓 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙌 Contributing

Contributions, bug reports, and suggestions are welcome!  
Feel free to fork the repo, open an issue, or submit a pull request.

---

## 📷 Screenshots (Optional)

Add photos/gifs of the project here for better understanding!

---

## 💬 Credits

Made with ❤ by [Your Name / GitHub Handle]  
Inspired by the open-source Wi-Fi security community.
