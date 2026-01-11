# 🛡️ DriverGuard: Intelligent Fatigue & Stress Detection System

An advanced, real-time AI monitoring system designed to enhance road safety. By leveraging Convolutional Neural Networks (CNN) and Computer Vision, DriverGuard detects early signs of driver exhaustion and emotional distress, providing instant life-saving alerts.

## 🌍 Real-World Impact
Driver exhaustion and emotional instability are primary contributors to global road fatalities. We developed this system as a **real-world solution** to be integrated into modern vehicle safety suites. Our goal is to **bridge the gap between AI research and road safety**, proactively preventing accidents before they occur.

## 📺 Project Demo
*(Upload your video to GitHub or YouTube and paste the link below)*
[![Project Demo](https://img.shields.io/badge/Demo-Video-red?style=for-the-badge&logo=youtube)]



https://github.com/user-attachments/assets/b39df453-283e-4bc1-b0e2-34db1486c2d8


## 👤 Project Information
- **Authors:** [Imran Mansor / Group 7]
- **Course:** STINK3014 Neural Networks (A251)
- **Institution:** Universiti Utara Malaysia (UUM)
- **Documentation:** [📄 View Full Project PDF](STINK3014_A251_Project/STINK3014_A251_GroupProject.pdf)

---

## 🚀 Advanced Features

### 1. Multi-State Emotion Detection (Stress Analysis)
Unlike standard systems, DriverGuard specifically isolates high-risk emotional states that lead to "aggressive" or "absent" driving:
*   **Fear & Surprise:** Indicates sudden road hazards or panic.
*   **Sadness & Disgust:** Monitors for emotional distraction and cognitive load.

### 2. Fatigue & Yawn Monitoring
*   **Eye Aspect Ratio (EAR):** Tracks eye closure duration to detect micro-sleeps.
*   **Yawn Counter:** Automatically increments a counter when frequent yawning is detected, a key physiological indicator of fatigue.

### 3. Dynamic "Bento-Style" Dashboard
A modern, dark-themed UI built with **Tailwind CSS** and **Chart.js** featuring:
*   **Fatigue Trend Line:** Real-time graph showing fatigue levels over time.
*   **Live Status HUD:** Visual indicators (Arrows/Circles) that light up when the driver looks away or is distracted.
*   **Live System Logs:** A scrolling terminal-style log of every system detection.

### 4. Real-Time Calibration (Surgical Tuning)
Adjust the system's sensitivity on the fly without restarting the code:
*   **Sensitivity Threshold:** Tune how easily the AI triggers an alert.
*   **Processing Speed:** Adjust the "Beta" smoothing factor for the fatigue algorithm.

### 5. Automatic Evidence Logging
When a violation (Critical Fatigue/Stress) is detected, the system:
*   Captures a **snapshot (.jpg)** of the driver.
*   Saves the event to a **Session CSV**.
*   Displays the evidence in the "Snapshots" gallery for post-trip review.

### 6. Post-Session AI Summary
Upon finishing a session, the system calculates:
*   **Driver Safety Score (0-100):** Based on total alerts and "Safe" time.
*   **AI Recommendations:** Personalized advice (e.g., "Take a break every 2 hours" or "High stress—try breathing exercises").

---

## 🛠️ Tech Stack
*   **Backend:** Python 3.9, Flask (Threaded Streaming)
*   **Machine Learning:** TensorFlow, Keras (CNN), OpenCV (Haar Cascades)
*   **Frontend:** HTML5, Tailwind CSS, JavaScript (ES6), Chart.js
*   **Data Handling:** NumPy, Pandas, CSV logging

---

## 📂 Project Structure
```text
DRIVER FATIGUE SYSTEM/
├── flask_driver_app/
│   ├── static/snapshots/      # Captured violation images
│   ├── templates/             # Dashboard, Summary, and Evidence HTML
│   ├── app.py                 # Flask Server & Logic
│   └── camera.py              # AI Vision Engine
├── STINK3014_A251_Project/
│   ├── STINK3014_A251_GroupProject.pdf  # Project Documentation
│   └── Pack01a_BaselineCode/  # CNN Model Training Scripts
├── stress_detector_cnn_improved.h5      # Trained AI Model
└── .gitattributes             # Git LFS Configuration
```

## ⚙️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/mern64/DriverGuard.git
   cd DriverGuard
   ```

2. **Run the application:**
   ```bash
   cd STINK3014_A251_Project/flask_driver_app
   python app.py
   ```
   Access the dashboard at `http://127.0.0.1:5001`.

---
*Note: The large training dataset (fer2013.csv) is excluded from this repository to maintain performance. The trained model is included and ready for use.*
