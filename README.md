# IoT25-HW06: ESP32 Web Server to Control GPIO Outputs

This project implements a standalone **ESP32-based Web Server** that allows users to control two GPIO pins (GPIO 26 and GPIO 27) from a web interface hosted on the ESP32 itself. The project uses HTML/CSS to create a simple UI for toggling LEDs or other connected actuators.

---

## 🧾 Objectives

- Set up an ESP32 to operate as a Wi-Fi access point or connect to a local network
- Host a web server on ESP32
- Control GPIO pins (e.g. LEDs) via HTTP requests
- Build a web interface using raw HTML + CSS served by ESP32

---

## 🧰 Components Used

- ESP32 DevKit v1  
- 2× LEDs (or other output devices)  
- Jumper wires  
- Breadboard  
- Smartphone or Laptop (for accessing the web interface)  

---

## 🌐 Web Interface Overview

- The ESP32 creates a Wi-Fi connection using:
  - SSID: `WiFi Name`  
  - Password: `password`
- Once connected, it starts an HTTP server on **port 80**
- The server listens for the following routes:
  - `/26/on` or `/26/off`: Controls GPIO 26
  - `/27/on` or `/27/off`: Controls GPIO 27
- Web page is served dynamically with button states and CSS styling

---

## 💡 Code Summary

- Uses the `WiFi.h` library to establish the network connection
- Uses `WiFiServer` and `WiFiClient` to handle HTTP requests
- HTML and CSS are sent as raw strings from ESP32 to the client
- Button presses change the GPIO output state and update the webpage

Example Behavior:

```html
<p>GPIO 26 - State on</p>
<p><a href="/26/off"><button class="button button2">OFF</button></a></p>
```

---

## 📸 Hardware Setup Photos

- ![Setup Photo 1](./media/hw%206-1.png)  
- ![Setup Photo 2](./media/hw%206-2.png)  
- ![Setup Photo 3](./media/hw%206-3.png)

---

## ▶ Demo

![Demo GIF](./media/IoT25-HW06.gif)  
(Also available as [video](./media/IoT25-HW06.mp4))

---

## ✅ Results

- [x] ESP32 connects to Wi-Fi and starts server successfully  
- [x] Buttons on webpage control GPIO 26 and 27 in real-time  
- [x] Web interface dynamically updates the state of outputs  
- [x] Compatible with smartphone or laptop browsers  

---

## 🔗 Reference
Rui Santos, VSCode + PlatformIO IDE: ESP32 & ESP8266, Arduino (Random Nerd Tutorials)
(https://randomnerdtutorials.com/esp32-web-server-arduino-ide/)
