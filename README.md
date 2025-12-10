# I.V.C. (Instant Vital Checkup)
![Original_timeline](https://github.com/nksrivastavaa/Instant-Vital-Checkup-IVC-/blob/main/Canva_Images/5.png)
![new_timeline](https://github.com/nksrivastavaa/Instant-Vital-Checkup-IVC-/blob/main/Canva_Images/7.png)
![future](https://github.com/nksrivastavaa/Instant-Vital-Checkup-IVC-/blob/main/Canva_Images/8.png)
![flaws](https://github.com/nksrivastavaa/Instant-Vital-Checkup-IVC-/blob/main/Canva_Images/9.png)
<!-- Recommendation: Use a sleek image of a computer vision overlay on a patient -->

[![Hackathon](https://img.shields.io/badge/Event-RedBrick_Hacks_2022-red)](https://devpost.com/)
[![Status](https://img.shields.io/badge/Status-Prototype-blue)]()
[![Tech Stack](https://img.shields.io/badge/Tech-OpenCV_%7C_Python_%7C_ML-green)]()

> **Automating pre-consultation triage using Computer Vision and Non-Contact Vitals Monitoring.**

---

## 📋 Table of Contents
- [Overview](#-overview)
- [Problem Statement](#-problem-statement)
- [The Solution](#-the-solution)
- [System Architecture](#-system-architecture)
- [Tech Stack](#-tech-stack)
- [Limitations](#-limitations)
- [Future Roadmap](#-future-roadmap)
- [Team](#-team)

---

## 📖 Overview
**Instant Vital Checkup (I.V.C.)** is a computer-vision-based health screening system designed to alleviate hospital bottlenecks. By utilizing a multi-camera setup at registration desks, I.V.C. automatically captures and calculates a patient's vital statistics—height, weight, BMI, pulse, and body temperature—without physical contact or nurse intervention.

**Watch the Demo:** [YouTube Link](https://www.youtube.com/watch?v=vMLdz9zY4uw)

---

## 🚩 Problem Statement
Medical negligence and delays in attending to critical patients are often caused by administrative bottlenecks. 
*   **Inefficiency:** Patients visiting for minor issues often face long wait times for basic pre-requisite checks (vitals).
*   **Resource Drain:** Skilled nurses spend a significant portion of their shifts performing repetitive manual measurements.
*   **Cost:** Manual procedures incur higher operational costs and equipment wear.

Our goal was to automate the "Triage" phase of a hospital visit using standard optical sensors and Machine Learning.

---

## 💡 The Solution
I.V.C. integrates into the hospital registration workflow. As the patient fills out their personal details at the desk, our system performs a passive scan:

1.  **Non-Contact Monitoring:** No wearables or cuffs required.
2.  **Instant Reporting:** Vitals are calculated in real-time and appended to the patient's Electronic Medical Record (EMR).
3.  **Computer Vision:** Utilizes anthropometric analysis and rPPG (Remote Photoplethysmography).

---

## ⚙️ System Architecture
The system relies on a **Triple-Camera Setup** to ensure data accuracy:

| Component | Sensor Type | Function |
| :--- | :--- | :--- |
| **Camera 1** | Wide-Angle / Depth | Captures full-body frame to estimate **Height**, **Weight**, and **BMI** using skeletal estimation algorithms. |
| **Camera 2** | High-Res Macro | Focuses on the facial ROI (Region of Interest) to detect micro-blushes in skin color for **Pulse/Heart Rate** extraction (rPPG). |
| **Camera 3** | Infrared / Thermal | Measures thermal radiation to determine body **Temperature**. |

---

## 🛠 Tech Stack
*   **Core Language:** Python
*   **Computer Vision:** OpenCV (cv2), MediaPipe (for pose estimation)
*   **Machine Learning:** Scikit-Learn (Regression models for weight estimation based on BMI/Height data)
*   **Hardware:** Infrared Sensors, Webcams

---

## ⚠️ Limitations
As a hackathon prototype, the current iteration has the following constraints:
*   **Environmental Factors:** Lighting conditions heavily affect the accuracy of rPPG (pulse) and skeletal tracking.
*   **registration Proxy:** If a family member registers on behalf of a critical patient, the system cannot scan the actual patient.
*   **Accessibility:** The current fixed-camera setup may not accurately measure patients in wheelchairs or those with severe physical deformities.

---

## 🚀 Future Roadmap
*   **Global Scalability:** Deploy as a SaaS API for hospital management software.
*   **Diagnostics:** Expand the CV model to detect visible structural deformities (e.g., Scoliosis) or dermatological symptoms.
*   **Predictive AI:** Integrate historical data to flag potential risks (e.g., "Patient has high temp + high pulse -> High Priority").

---

## 👥 Team LKC
*   **Dhruv Mishra**
*   **Krishnam Omar**
*   **Neelabh Kumar Srivastava**
*   **Priyanshu**
*   **Utkarsh Pal**

---
*Created for RedBrick Hacks 2022*
