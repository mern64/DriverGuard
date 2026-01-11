# 🛡️ DriverGuard: Intelligent Fatigue & Stress Detection System

An advanced, real-time AI monitoring system designed to enhance road safety. By leveraging Convolutional Neural Networks (CNN) and Computer Vision, DriverGuard detects early signs of driver exhaustion, distraction, and emotional distress, providing instant life-saving alerts.

> **⚠️ Note: Project Evolution**
> This project is a continuation and significant technical improvement of my previous work, [Driver Stress Detection](https://github.com/mern64/Driver-Stress-Detection)


> While the core CNN logic for stress analysis remains, **DriverGuard** transforms the concept into a fully deployable product. It introduces a responsive web dashboard, real-time distraction tracking, emergency SOS protocols, and post-trip analytics.

## 🌍 Real-World Impact

Driver exhaustion and emotional instability are primary contributors to global road fatalities. We developed this system as a **real-world solution** to be integrated into modern vehicle safety suites. Our goal is to **bridge the gap between AI research and road safety**, proactively preventing accidents before they occur.

## 📺 Project Demo

[https://github.com/user-attachments/assets/b39df453-283e-4bc1-b0e2-34db1486c2d8](https://github.com/user-attachments/assets/b39df453-283e-4bc1-b0e2-34db1486c2d8)

## 👤 Project Information

* **Authors:** [Imran Mansor / Group 7]
* **Course:** STINK3014 Neural Networks (A251)
* **Institution:** Universiti Utara Malaysia (UUM)
* **Documentation:** [📄 View Full Project PDF](https://www.google.com/search?q=STINK3014_A251_Project/STINK3014_A251_GroupProject.pdf)

---

## 🚀 Key Improvements & Features

Unlike standard detection systems, DriverGuard includes advanced "Real-World" capabilities:

### 1. Web-Based "Bento" Dashboard

Moved from a simple OpenCV window to a responsive **Flask + TailwindCSS** web interface.

* **Live Status HUD:** Visual overlays on the video feed indicating head direction (Left/Right) and warnings.
* **Real-Time Graph:** Tracks fatigue levels dynamically using Chart.js.

### 2. Multi-State Detection Logic

The system now detects four distinct driver states rather than just "Awake" or "Asleep":

* **Safe:** Normal driving behavior.
* **Drowsy:** Moderate fatigue detected (Yellow Warning).
* **Critical Fatigue:** sustained eye closure (Red Alert).
* **Distracted:** Head turning left/right or looking down/away.

### 3. Intelligent Yawn Counter

We implemented time-series analysis to distinguish yawns from other facial movements.

* **Logic:** Tracks mouth opening for specific duration frames (15-50 frames) to count yawns accurately.
* **Visual:** Displays a live "Yawn Count" badge on the dashboard.

### 4. Emergency SOS Simulation

A safety protocol for critical situations.

* **Trigger:** If fatigue remains >90% for a sustained period (microsleep).
* **Action:** Simulates sending an emergency message and locks the system into "SOS Mode" until reset.

### 5. Heads-Up Display (HUD) & Distraction Tracking

Visual cues overlaid directly on the camera feed.

* **Glowing Arrows:** Indicate when the driver looks too far Left or Right.
* **Status Indicators:** Visual text warnings ("EYES ON ROAD", "LOOKING AWAY").

### 6. Evidence Locker & Report Card

* **Auto-Capture:** Automatically saves a snapshot (`.jpg`) whenever a violation occurs.
* **Post-Session Analysis:** Generates a "Report Card" with a safety grade (A-F), total violation count, and AI-driven recommendations based on the drive.

---

## 🛠️ Tech Stack

* **Backend:** Python 3.9, Flask (Threaded Streaming)
* **Machine Learning:** TensorFlow, Keras (CNN), OpenCV (Haar Cascades)
* **Frontend:** HTML5, Tailwind CSS, JavaScript (ES6), Chart.js
* **Data Handling:** NumPy, Pandas, CSV logging

---

## 📂 Project Structure

```text
DRIVER FATIGUE SYSTEM/
├── flask_driver_app/
│   ├── static/snapshots/      # Captured violation images
│   ├── templates/             # Dashboard, Summary, and Evidence HTML
│   ├── app.py                 # Flask Server & Logic
│   └── camera.py              # AI Vision Engine & SOS Logic
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
