# RFID Attendance System (ESP32 + MFRC522 + Real-Time Clock)

## 📌 Overview
This project is an **RFID-based Attendance System** implemented on an ESP32 board with an MFRC522 RFID reader and a Real-Time Clock (RTC) for accurate timestamping.  
It allows users to **mark attendance by scanning RFID cards**, and the records can be viewed through a **built-in web interface**.

---

## ✅ Features
✔️ RFID Card Authentication  
✔️ Web-based Attendance Dashboard  
✔️ Real-Time Clock (RTC) for accurate Date & Time  
✔️ Buzzer & LED Feedback for Scan Status  
✔️ Stores Timestamp for Each User  
✔️ Simple and Responsive HTML UI  

---

## 🛠 Components Used
- **ESP32 Development Board**
- **MFRC522 RFID Reader**
- **RTC Module (DS3231 or similar)**
- **RFID Cards/Tags**
- **Buzzer**
- **LED**
- **WiFi Network**

---

## 📂 Project Structure

---

## ⚡ How It Works
1. ESP32 connects to your WiFi network.
2. The MFRC522 RFID module scans the card/tag.
3. If UID is authorized:
   - Attendance is marked with **Name, ID, Date & Time** (fetched from RTC)
   - Buzzer and LED provide success feedback
4. Web server provides:
   - **Home Page** – Welcome screen with links
   - **Attendance Page** – Shows all users who have marked attendance with real-time timestamps

---

## 🌐 Web Interface Screenshots
### ✅ Home Page
![Home Page](images/homepage.jpg)

### ✅ Attendance Page
![Attendance Page](images/Attendancepage.jpg)

---

## 🖼 Circuit Diagram
![Circuit Diagram](images/circuitdiagram.png)

---

## 📷 Implementation
![Implementation](images/implementation.jpg)

---

## ▶️ Working Video
[Click to view working video](workingvideo.mp4)

---

## 📋 How to Use
1. Download and install **Arduino IDE**.
2. Install required libraries:
   - `WiFi.h`
   - `SPI.h`
   - `MFRC522.h`
   - `WebServer.h`
   - `RTClib.h` (for DS3231 RTC)
3. Update your WiFi credentials in the code:
   ```cpp
   const char* ssid = "YOUR_WIFI_SSID";
   const char* password = "YOUR_WIFI_PASSWORD";

