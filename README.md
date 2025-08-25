# WiFi Security – DeAuthentication Attack Detector 🔒

This project is a prototype for detecting WiFi DeAuthentication (DeAuth) attacks in real-time using NodeMCU and other IoT hardware components.  
It aims to enhance **WLAN security** by alerting users whenever a malicious DeAuth frame is detected in the network.

---

## 🚀 Features
- Detects **DeAuth frames** in WiFi traffic  
- Provides **visual alert** via LED when an attack occurs  
- Uses **NodeMCU + TP-Link WiFi Adapter** for packet monitoring  
- Lightweight and portable prototype design  
- Supports **packet injection & scanning hidden networks**  

---

## 🛠️ Tools & Technologies
- **NodeMCU (ESP8266/ESP32)** – IoT device for detection logic  
- **TP-Link TL-WN722N** – WiFi adapter with packet injection support  
- **Arduino IDE** – Code compilation and flashing to NodeMCU  
- **C Programming** – Detection algorithm implementation  
- **Airmon-NG (Kali Linux)** – For scanning SSIDs and injecting test packets  
- **Breadboard & Jumper Wires** – Hardware prototyping  

---

## ⚙️ Installation & Setup
1. Clone this repository:
git clone https://github.com/saurav0607/WIFI-Security.git
Open the code in Arduino IDE.

Select the correct Board (NodeMCU ESP8266/ESP32) and Port.

Connect the NodeMCU via USB and upload the sketch.

Assemble the hardware:

Connect LED to NodeMCU via breadboard & jumper wires.

Plug in TP-Link adapter (for packet injection).

Run tests by simulating a DeAuth attack using:
airmon-ng start wlan0
aireplay-ng --deauth 10 -a <Router-MAC> wlan0
If attack is detected, the LED will light up as an alert.

📊 Prototype Workflow
Monitoring: WiFi adapter scans packets in real-time.

Detection: Code running on NodeMCU checks for DeAuth frames.

Alert: If attack is found → LED indicator turns ON.

Feedback: Logs and results are analyzed for improvements.

🔮 Future Improvements
Reduce detection latency
Add mobile notification support (via MQTT/IoT platforms)

Improve firmware to detect multiple attack types

Optimize cost for wider usability

---

👤 Author

Developed by Saurav Pokhrel

🎓 Postgraduate in Computer System Technology & Networking (Centennial College)

🎓 Bachelor’s in Ethical Hacking & Cybersecurity (Coventry University)


