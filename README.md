# KreoAssist  
Offline-First Disaster Management & Emergency Assistance Prototype

---

## 📌 Overview

KreoAssist is an offline-first disaster management and emergency assistance application designed for scenarios where conventional communication infrastructure becomes unreliable or unavailable.

The application focuses on **resilience, decentralization, and rapid response** by combining device-to-device mesh communication, hybrid AI-based assistance, and direct emergency actions.  
The current implementation serves as a **functional prototype**, validating critical emergency workflows under real-world constraints rather than aiming for full production deployment.

---

## 🧪 Prototype Status

KreoAssist is implemented as a working prototype with emphasis on **reliability, offline operation, and correctness** during emergency conditions.

### Implemented Prototype Capabilities
- Offline device-to-device communication via mesh networking
- Hybrid AI assistance with automatic online/offline switching
- One-tap SOS triggering with GPS-based emergency alerts
- Offline-accessible first-aid guidance for common medical emergencies

System scalability, extended integrations, and governance-level deployment considerations are **intentionally planned for the next round**.

---

## 🎯 Problem Statement (Governance Context)

During disasters such as floods, earthquakes, fires, and large-scale accidents:

- Mobile networks may fail or become congested
- Emergency instructions are delayed or inaccessible
- Verified first-aid guidance is unavailable at critical moments
- Centralized systems become single points of failure

KreoAssist addresses these challenges by enabling **decentralized communication, offline intelligence, and rapid local coordination**, aligning with governance-driven disaster response and public safety objectives.

---

## 🌟 Core Features

### 📡 Offline Mesh Communication
- Enables communication without internet using Bluetooth and Wi-Fi Direct
- No dependency on central servers
- Broadcast emergency states such as:
  - NEED HELP
  - I’M SAFE
  - Custom alerts
- Designed to remain operational in network blackout zones

![Mesh Network Interface](docs/screenshots/mesh_network.jpg)

---

### 🧠 Hybrid AI Emergency Assistant (Online + Offline)
- Automatically selects between online inference and on-device models
- Provides first-aid and emergency guidance (CPR, burns, fractures, choking)
- Supports offline processing for privacy and reliability
- Ensures assistance remains available during complete connectivity loss

![AI Assistant Screen](docs/screenshots/ai_assistant.jpg)

---

### 🆘 Emergency SOS Dashboard
- One-tap SOS triggers:
  - Emergency calls to national services (112)
  - SMS alerts containing precise GPS coordinates to trusted contacts
- Dedicated direct-dial buttons:
  - Police (100)
  - Fire (101)
  - Ambulance (102)
- Quick safety-status broadcasts for rapid coordination

![Emergency SOS Screen – Main](docs/screenshots/sos_dashboard.jpg)

![Emergency SOS Screen – Emergency Services](docs/screenshots/emergency_sos.jpg)

---

### 🏥 Offline First-Aid Guide
- Step-by-step instructions for common emergency scenarios
- Categorized access for rapid navigation
- Fully functional without internet connectivity
- AI-assisted follow-up questions when available

![Offline First Aid Guide](docs/screenshots/first_aid_guide.jpg)

---

## 🎨 Design Considerations

- AMOLED-optimized dark theme for reduced battery usage
- Minimal, stress-aware UI design for emergency situations
- Optimized animations for modern mobile devices
- Focus on usability under panic and low-visibility conditions

---

## 🔁 System Flow & Data Flow Diagrams (Round-1 Requirement)

This section documents the **technical flow charts and data flow diagrams** describing how KreoAssist operates during emergency scenarios.

### 1️⃣ System Flow Chart (High-Level Application Flow)

This flow chart represents the end-to-end execution path of the application under both online and offline conditions.

Flow description:
- User interacts with the application UI
- Connectivity manager determines network availability
- AI requests are routed to:
  - Online inference service (if available), or
  - On-device AI model (offline mode)
- SOS actions trigger GPS retrieval, emergency calls, and alerts
- Emergency packets are broadcast to nearby devices via mesh networking
- Mesh nodes propagate safety status locally

![System Flow Diagram](docs/screenshots/system_flow.png)

---

### 2️⃣ SOS Data Flow Diagram (DFD)

This DFD illustrates how emergency data moves through the system after an SOS is initiated.

Data flow:
- User initiates SOS
- GPS module provides location coordinates
- SOS handler performs:
  - Emergency call execution
  - SMS delivery to trusted contacts
- SOS message payload is broadcast over the mesh network
- Nearby devices receive and display emergency status updates

![SOS Data Flow Diagram](docs/screenshots/sos_dfd.png)

---

## 🧩 System Architecture & Technical Flow

KreoAssist follows a modular architecture designed to support both online and offline execution paths.

- User actions originate from the interface layer
- Connectivity manager controls online/offline routing
- AI engine processes queries based on connectivity
- SOS handler manages emergency signaling
- Mesh controller distributes messages to nearby devices

![System Architecture Diagram](docs/screenshots/system_architecture.png)

---

## 🛠️ Technology Stack

- Framework: Flutter (Dart)
- State Management: Riverpod
- Connectivity: Bluetooth and Wi-Fi Direct (mesh networking)
- Location Services: Device GPS
- Emergency Handling: Direct phone call and SMS APIs
- Offline Intelligence: On-device language model inference
- Online Intelligence: External inference service (used only when available)

---

## 📁 Project Structure

- lib/  
  Core application logic including UI layers, state management, mesh networking, AI handling, and SOS workflows

- assets/  
  Offline first-aid data, images, and static resources

- docs/  
  Architecture diagrams and technical documentation

Other platform-specific directories (android, ios, macos) follow standard Flutter project conventions.

---

## 🚀 Planned Enhancements for Round 2

In Round 2, KreoAssist will be expanded from a functional prototype into a more **scalable and governance-ready emergency platform**.

### 1. Scalability & Network Reliability
- Message prioritization (SOS over non-critical updates)
- Message expiration (TTL) to reduce mesh congestion
- Battery-aware communication optimization

### 2. Advanced Offline Navigation
- Integration of offline maps using OpenStreetMap
- Geo-tagged Safe Zones and Danger Zones
- Local route guidance based on available safety data

### 3. Governance & Official Integration
- Integration with official disaster alert sources when connectivity is available
- Standardized emergency data formats for interoperability with public systems

### 4. Accessibility & Inclusivity
- Support for regional Indian languages
- Voice-triggered SOS and guidance for injured or visually impaired users

### 5. Extended Communication (Experimental)
- Exploration of long-range communication using LoRa-based hardware
- Integration with IoT sensors for automated hazard detection and alerts

---

## 👥 Team

This project is developed collaboratively by a hackathon team, Kreodev.  
Contributions include application development, system design, and documentation.

---

## 📄 Notes

This repository represents a hackathon prototype focused on validating emergency workflows under real-world constraints.  
The project prioritizes resilience, offline operation, and governance-aligned disaster response.

---

© 2025 Kreodev. All rights reserved.