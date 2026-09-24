# 🧤 Smart Sign Language Gloves

### Offline, App-Free Sign Language to Speech Wearable

> **Giving a voice to the voiceless, instantly.**

An **offline and app-free smart wearable glove** designed to translate sign language into spoken audio in real time. The system uses **ESP32-C3, capacitive touch sensors, MPU6050 motion tracking, edge computing, a local web server, WebSockets, and 3D visualization** to provide an accessible communication solution.

---

## 📌 Overview

People who communicate using sign language may face difficulties when interacting with people who do not understand sign language.

The **Smart Sign Language Gloves** project aims to reduce this communication barrier by detecting hand signs and converting them into spoken output.

The glove uses a **5-bit binary touch system** to detect finger/touch patterns. An **MPU6050 motion sensor** is used to verify intentional hand movement and reduce false detections.

The ESP32-C3 processes the input locally and provides a web interface without requiring an internet connection or a dedicated mobile application.

---

## ✨ Key Features

* 📴 **Offline Operation** – Works without internet connectivity.
* 📱 **App-Free Interface** – Access the system through a web browser.
* 👆 **5-Bit Binary Touch Detection** – Detects sign patterns using capacitive touch sensors.
* 🧭 **MPU6050 Motion Tracking** – Detects and verifies hand movement.
* 🛡️ **Anti-Misfire Detection** – Combines touch and motion information.
* ⚡ **Edge Computing** – Processes data locally on the ESP32-C3.
* 🌐 **Local Web Server** – ESP32-C3 hosts the interface locally.
* 🔄 **WebSocket Communication** – Enables real-time communication.
* 🎨 **3D Visualization** – Displays live glove/sign information.
* 🔊 **Text-to-Speech Output** – Converts recognized signs into spoken audio.

The project documentation specifically identifies capacitive touch sensing, MPU6050 motion tracking, ESP32-C3 processing, local web serving, WebSockets, Three.js visualization, and native TTS as core technologies.

---

## 🛠️ Hardware Components

| Component                       | Purpose                                       |
| ------------------------------- | --------------------------------------------- |
| ESP32-C3                        | Main microcontroller and edge-processing unit |
| TTP223 Capacitive Touch Sensors | Detect touch/finger states                    |
| MPU6050                         | Motion and movement tracking                  |
| Smart Glove                     | Wearable platform                             |
| Power Management                | Portable power supply                         |

The prototype is based on an ESP32-C3 with TTP223 capacitive touch sensors and MPU6050 motion tracking.

---

## 💻 Technologies Used

* **ESP32-C3**
* **Embedded C/C++**
* **HTML**
* **CSS**
* **JavaScript**
* **WebSockets**
* **Three.js**
* **Text-to-Speech**
* **Edge Computing**
* **Sensor Fusion**
* **Local Wi-Fi**

---

## 🔄 Working Principle

```text
          POWER ON
              │
              ▼
      ESP32-C3 Creates
       Local Wi-Fi
              │
              ▼
      Connect Using Phone
         Web Browser
              │
              ▼
     Capacitive Touch Input
              │
              ▼
       5-Bit Binary Pattern
              │
              ▼
       MPU6050 Motion Check
              │
              ▼
      Sensor Fusion / 
      Anti-Misfire Logic
              │
              ▼
       Sign Recognition
              │
              ▼
       WebSocket Transfer
              │
              ▼
       3D Web Dashboard
              │
              ▼
       Text-to-Speech
              │
              ▼
        Spoken Output
```

The documented workflow is **Power On → Connect → Form Sign → Swipe → Output**.

---

## 🧠 How It Works

### 1. Power ON

The ESP32-C3 starts the glove system and creates its own local Wi-Fi network.

### 2. Connect

A smartphone connects to the glove's local network and opens the web interface through a browser.

No dedicated mobile application or internet connection is required.

### 3. Touch Detection

The TTP223 capacitive touch sensors detect the user's touch/finger states.

These inputs are represented as a **5-bit binary pattern**.

### 4. Motion Verification

The MPU6050 tracks hand movement.

The motion information is combined with the touch information to verify intentional gestures and reduce accidental detections.

### 5. Sign Recognition

The ESP32-C3 processes the sensor information locally and determines the corresponding sign.

### 6. WebSocket Communication

The recognized information is transmitted through asynchronous WebSocket communication.

### 7. Visualization

A local web dashboard provides visualization of the detected information using **Three.js**.

### 8. Speech Output

The recognized sign is converted into spoken audio using text-to-speech functionality.

---

## 🏗️ System Architecture

```text
 ┌──────────────────────────┐
 │ Capacitive Touch Sensors │
 │         TTP223           │
 └────────────┬─────────────┘
              │
              ▼
 ┌──────────────────────────┐
 │        ESP32-C3          │
 │    Edge Processing       │
 └────────────┬─────────────┘
              ▲
              │
 ┌────────────┴─────────────┐
 │         MPU6050           │
 │     Motion Tracking      │
 └───────────────────────────┘
              │
              ▼
 ┌──────────────────────────┐
 │   Sensor Fusion &        │
 │   Anti-Misfire Logic     │
 └────────────┬─────────────┘
              │
              ▼
 ┌──────────────────────────┐
 │   Local Web Server &     │
 │       WebSockets         │
 └────────────┬─────────────┘
              │
              ▼
 ┌──────────────────────────┐
 │    3D Web Dashboard      │
 │       Three.js           │
 └────────────┬─────────────┘
              │
              ▼
 ┌──────────────────────────┐
 │     Text-to-Speech       │
 │      Spoken Output       │
 └──────────────────────────┘
```

---

## 🌐 Offline & App-Free Communication

A major feature of the project is its **offline and app-free operation**.

The ESP32-C3 works as a local server and allows the user to access the interface through a smartphone browser.

```text
Smart Glove
     │
     │ Local Wi-Fi
     ▼
 Smartphone Browser
     │
     ▼
 Local Web Interface
```

This eliminates the requirement for:

* Internet connectivity
* Cloud services
* Dedicated mobile application
* External server infrastructure

---

## 💡 Innovation

The project combines multiple technologies into a single wearable system:

* Capacitive touch sensing
* Motion tracking
* Sensor fusion
* Edge computing
* Embedded systems
* Local web technologies
* WebSocket communication
* 3D visualization
* Text-to-speech

The proposed design replaces expensive and fragile flex sensors with capacitive touch pads, while MPU6050 motion tracking is used to help verify intentional hand movements.

---

## 💰 Cost Objective

According to the EUREKA 2026 proposal:

* **Prototype build cost:** Under ₹750
* **Target retail price:** ₹2,500

The objective is to develop an affordable assistive wearable while maintaining useful real-time functionality.

---

## 🎯 Target Users

The proposed target users include:

* Speech and hearing-impaired individuals
* Specialized schools
* Medical facilities
* NGOs
* Inclusive workplaces

The project documentation identifies speech/hearing-impaired individuals, specialized schools, and medical facilities as target customers.

---

## 📊 MVP Status

The project has reached a **functional Minimum Viable Product (MVP)** stage.

The MVP demonstrates:

* Offline operation
* App-free communication
* Sign detection
* Local web interface
* Real-time output

The proposal states that the MVP is ready for real-world user beta testing.

---

## 📷 Project Images

Add your project photographs and dashboard screenshots here.

```text
docs/
│
├── glove.jpg
├── hardware.jpg
├── circuit.jpg
├── dashboard.jpg
└── demonstration.jpg
```

Example:

```markdown
![Smart Sign Language Glove](docs/glove.jpg)
```

---

## 🎥 Demonstration

Add your project demonstration video or GIF here.

```markdown
[▶️ Watch Project Demonstration](YOUR_VIDEO_LINK)
```

---

## 🚀 Future Scope

Future improvements include:

* PCB miniaturization
* Improved ergonomic glove design
* Expanded sign vocabulary
* Improved recognition accuracy
* Larger user testing
* Commercial-ready prototype
* Mass manufacturing

The proposed next milestones include PCB miniaturization, ergonomic glove materials, and a 20-user pilot program.

---

## 👥 Team – IntelliX Titans

| Member                   | Contribution                       |
| ------------------------ | ---------------------------------- |
| **John Stewartsson J R** | Hardware / Firmware Development    |
| **Joshua Miracle J**     | Sensor Integration and Testing     |
| **Mahalakshmi P**        | HTML / CSS / JavaScript            |
| **Narmathakavi C S**     | 3D Integration and Hardware Design |

---

## 🏆 Project Information

| Category         | Details                    |
| ---------------- | -------------------------- |
| **Event**        | EUREKA 2026                |
| **Team**         | IntelliX Titans            |
| **Project**      | Smart Sign Language Gloves |
| **Domain**       | Assistive Technology       |
| **Platform**     | ESP32-C3                   |
| **System Type**  | Wearable / Edge Computing  |
| **Connectivity** | Local Wi-Fi                |
| **Operation**    | Offline                    |

---

## ⭐ Project Highlights

```text
✓ Offline Operation
✓ App-Free Communication
✓ ESP32-C3 Edge Computing
✓ 5-Bit Binary Touch Detection
✓ MPU6050 Motion Tracking
✓ Sensor Fusion
✓ Anti-Misfire Detection
✓ Local Web Server
✓ WebSocket Communication
✓ 3D Visualization
✓ Text-to-Speech
✓ Low-Cost Wearable
```

---

## 📌 Conclusion

The **Smart Sign Language Gloves** project demonstrates how embedded systems, wearable sensors, edge computing, and web technologies can be combined to create an accessible communication solution.

By providing **offline, app-free sign-to-speech translation**, the project aims to reduce communication barriers and make assistive technology more affordable and accessible.

---

## 📄 License

This project is developed as part of the **EUREKA 2026** project initiative by **IntelliX Titans**.

Add an appropriate open-source license if you plan to make the source code publicly reusable.
