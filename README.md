<div align="center">
       
# 💧 HyperMate
### *Smart Wellness Companion for Hyperhidrosis Management*

[![Flutter](https://img.shields.io/badge/Flutter-3.0+-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![ESP8266](https://img.shields.io/badge/ESP8266-IoT-E7352C?style=for-the-badge&logo=espressif&logoColor=white)](https://www.espressif.com)
[![OpenAI](https://img.shields.io/badge/OpenAI-GPT--3.5-412991?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com)

**A Freelance Flutter mobile application integrated with ESP8266 hardware to help people with hyperhidrosis (excessive sweating) manage their condition through real-time monitoring, personalized diet recommendations, relaxation exercises, and AI-powered support.**

[Features](#-key-features) • [Architecture](#-system-architecture) • [Tech Stack](#-tech-stack) • [Demo](#-demo)

<br>
<img width="400" alt="HyperMate Cover photo" src="https://github.com/user-attachments/assets/73ad992b-f80c-40e0-a0cf-189e9d540ac1" />



</div>

---

## 🎯 The Problem

**Hyperhidrosis** affects millions worldwide — causing excessive sweating that can be triggered by stress, anxiety, or certain foods. This condition:
- Creates dangerous situations (e.g., slippery hands while driving)
- Causes social anxiety and discomfort
- Has no simple cure, only management strategies

**Current solutions fall short:**
- Generic apps don't address the physical symptoms
- Medical devices are expensive and clinical
- No integrated approach combining diet, exercise, and real-time monitoring

---

## 💡 The Solution

**HyperMate** provides an integrated mobile + hardware solution:

| Component | Purpose |
|-----------|---------|
| 📱 **Flutter App** | Central hub for recommendations, tracking, and AI chat |
| 🔧 **ESP8266 Device** | Real-time GSR (sweat) sensor + cooling fan |
| 🤖 **AI Chatbot** | 24/7 emotional support via GPT-3.5 |
| 🎥 **Exercise Videos** | Curated relaxation content based on stress levels |

---

## 🎬 Demo

Watch the full system in action, including hardware integration:

[![HyperMate Demo](https://img.youtube.com/vi/I7HxB9zB4rE/maxresdefault.jpg)](https://youtu.be/I7HxB9zB4rE)

---

## ✨ Key Features

### 📊 Real-Time Sensor Monitoring
- Live GSR (Galvanic Skin Response) readings displayed on home screen
- Automatic data polling every second via Wi-Fi
- Visual ring indicator showing current sweat levels

### 🍽️ Personalized Diet Recommendations  
- Curated meal suggestions organized by time of day
- Foods scientifically linked to reducing sweating
- Clear warnings about trigger foods (caffeine, sugar, spicy)
- Personalized food quiz to tailor recommendations

### 🧘 Stress-Based Exercise Videos
- YouTube-integrated relaxation videos
- Video recommendations adapt based on sensor readings
- Embedded player with full playback controls

### 🤖 AI-Powered Chatbot ("Comfort Zone")
- GPT-3.5 integration for conversational support
- Persistent chat history using local storage
- Markdown-rendered responses for rich formatting

### ⚡ Hardware Companion (Optional)
- ESP8266 creates its own Wi-Fi access point
- GSR sensor measures skin conductivity (sweat indicator)
- PWM-controlled fan provides automatic cooling
- Standalone operation — no internet required

---

## 🏗 System Architecture

The system operates on a local Wi-Fi network created by the ESP8266, ensuring low latency for sensor data, while the app manages internet connectivity for AI features.

```
┌──────────────┐          ┌─────────────────────┐
│  FLUTTER APP │  Wi-Fi   │   ESP8266 DEVICE    │
│ (Client UI)  │ ◄──────► │ (AP Mode + Server)  │
└──────┬───────┘ HTTP API └──────────┬──────────┘
       │                             │
       │ HTTPS                       │ PWM / Analog
       ▼                             ▼
┌──────────────┐          ┌─────────────────────┐
│ OpenAI Human │          │  Sensors & Fan      │
│     API      │          │  (Hardware Layer)   │
└──────────────┘          └─────────────────────┘
```

---

## 🛠 Tech Stack

### Mobile Application
- **Framework**: Flutter (Dart)
- **State/UI**: `flutter_screenutil` for responsiveness
- **Remote Data**: `http` (Local IoT), `dart_openai` (Cloud AI)
- **Local Data**: `shared_preferences`
- **Media**: `youtube_player_flutter`

### Hardware
- **Microcontroller**: ESP8266 (NodeMCU)
- **Sensors**: GSR (Galvanic Skin Response)
- **Actuators**: DC Fan with L298N Driver
- **Protocol**: HTTP/1.1 REST Server over SoftAP

---
    
## 📱 Gallery

<div align="center">

### 🏠 Core & Hardware
| Dashboard | Hardware Setup | Real-time Measurement |
|:---:|:---:|:---:|
| <img src="readme_media/screenshots/Home%20Screen.jpeg" width="200" /> | <img src="readme_media/screenshots/Hardware%20connections.jpeg" width="200" /> | <img src="readme_media/screenshots/Measurement%20screen.png" width="200" /> |

### 🥗 Diet & Nutrition
| Food Categories | Detailed Recommendations | Trigger Warnings |
|:---:|:---:|:---:|
| <img src="readme_media/screenshots/Food%20List%20Screen%201.jpeg" width="200" /> | <img src="readme_media/screenshots/Food%20List%20Screen%202.jpeg" width="200" /> | <img src="readme_media/screenshots/Food%20List%20Screen%203.jpeg" width="200" /> |

### 📝 Personalization Quiz
| Diet Quiz | Quiz Summary |
|:---:|:---:|
| <img src="readme_media/screenshots/Quiz%20screen.png" width="200" /> | <img src="readme_media/screenshots/Quiz%20summary%20screen.png" width="200" /> |

### 🤖 AI Support & Relaxation
| Chatbot Intro | Conversational Support | Relaxation Videos |
|:---:|:---:|:---:|
| <img src="readme_media/screenshots/Smart%20Chatbot%20screen%201.jpeg" width="200" /> | <img src="readme_media/screenshots/Smart%20Chatbot%20screen%202.png" width="200" /> | <img src="readme_media/screenshots/Excercise%20screen%202.jpeg" width="200" /> |

</div>

---

## 📬 Client Feedback

<div align="center">

> "I liked how practical and focused you are, and how working with you always felt organized and goal-oriented. The given results were like how we wanted it."
> <br>— **Sama Wahba**

> "Through our discussions, he helped us identify some useful features to add such as the AI bot... The application was delivered with a highly professional finish."
> <br>— **Sandra Samir**

> "He takes his work seriously, providing clear communication to understand the client's needs... Willingness to give the best work."
> <br>— **Mariam Abdelhamid**

</div>

---

## 👨‍💻 Author

**Mamdouh Attia**  
Computer Engineer | Mobile Software Engineer

---
## 📝Copyright

This is a freelance project for a client and it is not for public use in the current time. The idea , app design, hardware and the app is owned by the client. My role was to develop the app and help with the hardware issues and the code , and the integration between the app and the hardware.

Copyright © 2026 HyperMate. All rights reserved.

---

## 📄 License


MIT License

