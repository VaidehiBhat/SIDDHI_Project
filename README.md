# SIDDHI: sEMG-Based Wearable System for Early Detection of Neuromuscular Disorders

This repository documents our multi-phase project conducted under **SIDDHI 2024** – Summer Internship for Data-Driven Healthcare Innovations. The project focuses on developing an integrated, low-cost, and non-invasive solution for the **early diagnosis and monitoring of neuromuscular disorders** (NMDs) using **surface EMG (sEMG) signals**.

---


---

## 🔬 Team7_SIDDHI24 (Part 1 – Software Model)

In this phase, we focused on building a **robust machine learning pipeline** for detecting early signs of neuromuscular anomalies based on open-source sEMG datasets.

Key contributions:
- Built a signal preprocessing pipeline including noise filtering, rectification, normalization
- Extracted statistical time- and frequency-domain features such as RMS, ZCR, Mean/Median Frequency, etc.
- Compared multiple anomaly detection algorithms including:
  - One-Class SVM
  - Isolation Forest
  - Elliptic Envelope
  - CNN-LSTM (for temporal modeling)
- Designed and deployed a web app for patient interaction with features like login, signal upload, report generation (PDF), and history tracking
- Proposed a One-Class SVM + Elliptic Envelope hybrid architecture for anomaly detection
- Built a patient-friendly dashboard for visualizing preprocessed EMG signals and ML results

📝 The outcomes of this phase formed the core of our **published research paper** (included in this repo).

---

## 🔧 SIDDHI2.0 (Part 2 – Hardware Extension)

This second phase focused on extending our ML-based detection model into a fully functional **wearable device**, incorporating real-time EMG signal acquisition, on-device preprocessing, and wireless transmission.

Key technical aspects:
- Developed a standalone, battery-powered sEMG device using:
  - **Techtonics EMG Muscle Sensor V3.0**
  - **ESP32 microcontroller** (for dual-core real-time processing and WiFi communication)
  - OLED display for real-time instructions and results
- Implemented a microcontroller-side logic to:
  - Collect EMG signals for 8-second sessions
  - Display muscle activity instructions via countdown timer
  - Save data in `.csv` format and transmit it to a cloud-based backend
- Designed analog front-end for signal conditioning
  - ±5V regulated dual power supply using LM7805, LM7905, or TJ7660 voltage inverter
  - Rechargeable 12V Li-ion battery circuit
- Cloud communication (planned) with AWS/Azure for ML inference and storage
- First-generation prototype successfully acquired and displayed EMG signals from users

---

## 🏆 Publication

The work in Phase 1 (Team 7) has resulted in a **research paper** (included) and served as the theoretical foundation for the wearable system in Phase 2.

---

## 📂 Files in This Repository

- `Team7_SIDDHI24_Presentation_Report.pdf` — Initial design, ML pipeline, and app interface  
- `SIDDHI2.0_Presentation_Report.pdf` — Wearable hardware prototype, microcontroller logic, signal examples  
- `One-Class_SVM_Using_Domain-Based_sEMG_Features_for_Detection_of_Neuromuscular_Disorders.pdf` — Formal paper based on our Phase 1 contributions

---

## 🔗 Acknowledgment

This project was carried out under the mentorship of **Dr. Hitendra Kumar** and **Dr. Vibhor Pandhare** as part of the **SIDDHI 2024 program** at the **Charak Center for Digital Healthcare, IIT Indore**.

---

