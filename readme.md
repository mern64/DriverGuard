# Driver Fatigue and Stress Detection System

An AI-powered monitoring system designed to enhance road safety by detecting driver fatigue and emotional stress in real-time. This project uses a Convolutional Neural Network (CNN) to analyze facial expressions and alert drivers when risky behavior is detected.

## 📺 Project Demo
*(Replace the link below with your actual video link)*
[![Project Demo](https://img.shields.io/badge/Demo-Video-red?style=for-the-badge&logo=youtube)](YOUR_VIDEO_LINK_HERE)

## 👤 Authors & Project Info
- **Lead Developer:** [Your Name/Group Name]
- **Course:** STINK3014 Neural Networks
- **Documentation:** [📄 View Project Report (PDF)](STINK3014_A251_Project/STINK3014_A251_GroupProject.pdf)

## 🚀 Key Features
- **Real-time Monitoring:** High-performance live camera feed processing via Flask.
- **Stress Detection:** The system specifically monitors for high-stress emotional states:
  - **Fear**
  - **Surprise**
  - **Sadness**
  - **Disgust**
- **Fatigue Tracking:** Real-time calculation of fatigue levels based on eye closure and yawn frequency.
- **Evidence Logging:** Automatically captures snapshots of violations and logs data to CSV for post-session analysis.
- **Interactive Dashboard:** A modern, bento-style web interface with live charts and system logs.

## 🛠️ Tech Stack
- **Backend:** Python 3.9, Flask
- **AI/ML:** TensorFlow, Keras, OpenCV (Haar Cascades)
- **Frontend:** HTML5, Tailwind CSS, Chart.js

## 📂 Project Structure
- `flask_driver_app/`: Main application logic (`app.py`) and UI templates.
- `STINK3014_A251_Project/`: 
  - `Pack01a_BaselineCode/`: Training scripts and model development.
  - `Pack01b_DeploymentCode/`: Production-ready scripts.
  - `STINK3014_A251_GroupProject.pdf`: Detailed project documentation and research findings.
- `stress_detector_cnn_improved.h5`: The optimized deep learning model.

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
