# 🚗 XR Car Racer

## 📌 Overview

XR Drift: Reality Racer is a Unity-based racing simulation enhanced with **Extended Reality (XR)** technologies.
The project transforms a traditional car racing system into an immersive experience using **Virtual Reality (VR)** and **Augmented Reality (AR)**.

* In **VR Mode**, players drive from a first-person cockpit using headset controls.
* In **AR Mode**, players place and control a miniature car on real-world surfaces using a mobile device.

---

## 🎯 Key Features

### 🚘 Core Racing System

* Realistic physics using Rigidbody and WheelColliders
* Torque-based acceleration and braking system
* Steering with smooth input handling
* AI racers with lap tracking and race positions

---

### 🥽 Virtual Reality (VR)

* First-person cockpit driving experience
* 360° head tracking
* Analog throttle using controller triggers
* XR Origin attached to car for synchronized movement
* World-space dashboard (speed, gear, RPM)

---

### 📱 Augmented Reality (AR)

* Real-world surface detection (plane detection)
* Tap-to-place car in physical environment
* Miniature car scaling for tabletop gameplay
* On-screen joystick controls
* Camera-based real-world integration

---

## 🧠 System Architecture

### 🔁 Game Loop

1. Input (Keyboard / VR Controllers / Touch)
2. CarStateMachine processes input
3. EngineController applies torque & gear logic
4. Physics simulation (Rigidbody + WheelColliders)
5. XR tracking updates camera
6. Rendering via URP (VR / AR / Screen)

---

### 🧩 Core Components

| Component        | Description                          |
| ---------------- | ------------------------------------ |
| CarStateMachine  | Central input and control handler    |
| EngineController | Handles torque, RPM, gear shifting   |
| WheelColliders   | Simulate tire physics and suspension |
| XR Origin        | VR camera rig attached to car        |
| VRCarInput       | Converts VR controller input         |
| ARTapToPlace     | Handles AR object placement          |

---

## 🥽 XR Integration (Main Contribution)

### 🔹 VR Implementation

* Integrated **OpenXR** for cross-platform VR support
* Attached XR Origin to car (parent-child transform system)
* Implemented analog throttle using trigger input
* Added fallback input system (VR + Keyboard compatibility)

---

### 🔹 AR Implementation

* Used **AR Foundation** for cross-platform AR
* Implemented plane detection and raycasting
* Created AR scene with AR Session + AR Origin
* Designed tap-to-place interaction system

---

## 🛠️ Technologies Used

* Unity 2022 LTS (URP)
* OpenXR
* XR Interaction Toolkit
* AR Foundation (ARCore / ARKit)
* C# (MonoBehaviour scripting)
* Unity Input System

---

## 🎮 Controls

### 🖥️ PC (Keyboard)

* W / S → Accelerate / Reverse
* A / D → Steering
* Space → Brake

---

### 🥽 VR

* Right Trigger → Throttle
* Left Trigger → Brake
* Left Joystick → Steering
* Head Movement → Camera

---

### 📱 AR (Mobile)

* Tap → Place car
* On-screen joystick → Control movement

---

## 🚀 Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/muhammad-anas-15/XR-Car-Racer.git
```

### 2. Open in Unity

* Recommended: Unity 2022 LTS
* Open project via Unity Hub

---

### 3. Enable XR

* Install XR Plugin Management
* Enable OpenXR (PC platform)
* Add controller interaction profiles

---

### 4. Install AR Support

* Install AR Foundation
* Install ARCore (Android) or ARKit (iOS)

---

### 5. Open Scenes

* `MainRace.unity` → VR / PC gameplay
* `ARScene.unity` → AR mode

---

## 🧪 Testing

### Without Hardware

* Use XR Device Simulator
* Mouse = Head movement
* Keyboard = Driving

---

### With Hardware

* VR: Oculus Quest / HTC Vive / Valve Index
* AR: Android (ARCore) / iOS (ARKit)

---

## ⚡ Performance Optimization

### VR

* Target 90 FPS
* Use baked lighting
* Enable single-pass rendering
* Avoid real-time lights

---

### AR

* Limit polygon count (<10k)
* Disable shadows
* Use mobile texture compression

---

## 🔮 Future Improvements

* VR steering wheel interaction (grab-based control)
* AI traffic system improvements
* Multiplayer support
* Realistic tire physics (advanced models)
* AR occlusion & real-world lighting

---

## 🙏 Credits

This project is based on an open-source Unity car racing system developed by:

* besnik420
* Coding_edge

### ✨ My Contribution

I extended the original project by implementing:

* VR cockpit experience using OpenXR
* AR tabletop gameplay using AR Foundation
* XR input bridging system
* Dual-mode gameplay architecture (VR + AR)

---

## 📢 Note

This project demonstrates how an existing game system can be enhanced with XR technologies by modifying camera systems, input handling, and interaction design without altering core physics.

---
