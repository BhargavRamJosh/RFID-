# RFID Attendance System (ESP32 + MFRC522)

## 📌 Overview
This project is an **RFID-based Attendance System** implemented on an ESP32 board with an MFRC522 RFID reader.  
It allows users to **mark attendance by scanning RFID cards**, and the records can be viewed through a **built-in web interface**.

---

## ✅ Features
✔️ RFID Card Authentication  
✔️ Web-based Attendance Dashboard  
✔️ Buzzer & LED Feedback for Scan Status  
✔️ Stores Timestamp for Each User  
✔️ Simple and Responsive HTML UI  

---

## 🛠 Components Used
- **ESP32 Development Board**
- **MFRC522 RFID Reader**
- **RFID Cards/Tags**
- **Buzzer**
- **LED**
- **WiFi Network**

---

## 📂 Project Structure
RFID_Attendance_System/
│
├── RFID_Attendance.ino # Main Arduino Code
├── README.md # Project Documentation
├── images/ # Screenshots of Web UI
│ ├── home_page.png
│ ├── attendance_page.png
│ └── access_denied.png

---

## ⚡ How It Works
1. ESP32 connects to your WiFi network.
2. The MFRC522 RFID module scans the card/tag.
3. If UID is authorized:
   - Attendance is marked with **Name, ID, Date & Time**
   - Buzzer and LED provide success feedback
4. If UID is unauthorized:
   - Displays **Access Denied** page
   - Buzzer alerts user
5. Web server provides:
   - **Home Page** – Welcome screen with links
   - **Attendance Page** – Shows all users who have marked attendance
   - **Status Pages** – Success or Access Denied message

---

## 🌐 Web Interface Screenshots
### ✅ Home Page
![Home Page](images/home_page.png)

### ✅ Attendance Page
![Attendance Page](images/attendance_page.png)

### ✅ Access Denied Page
![Access Denied](images/access_denied.png)

---

## 📋 How to Use
1. Download and install **Arduino IDE**.
2. Install required libraries:
   - `WiFi.h`
   - `SPI.h`
   - `MFRC522.h`
   - `WebServer.h`
3. Update your WiFi credentials in the code:
   ```cpp
   const char* ssid = "YOUR_WIFI_SSID";
   const char* password = "YOUR_WIFI_PASSWORD";
