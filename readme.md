# Driver Fatigue and Stress Detection System

An AI-powered monitoring system designed to enhance road safety by detecting driver fatigue and emotional stress in real-time. This project uses a Convolutional Neural Network (CNN) to analyze facial expressions and alert drivers when risky behavior is detected.

## 📺 Project Demo
*(Upload your video to GitHub or YouTube and paste the link here)*
[![Project Demo](https:/![23DEFCED-126B-48DD-B590-ADFCBAF9355F_1_102_o](https://github.com/user-attachments/assets/0e09a64d-cf1c-4071-a8d3-5cef206e6b22)
/img.shields.io/badge/Demo-Video-red?style=for-the-badge&logo=youtube)](Uploading DriverGuard Demo.mov…)
## 🚀 Features
- **Real-time Monitoring:** Live camera feed processing via Flask.
- **Stress Detection:** Specifically identifies: **Fear, Surprise, Sadness, and Disgust**.
- **Fatigue Tracking:** Monitors for signs of tiredness and lack of focus.
- **Evidence Logging:** Automatically captures snapshots and logs session data into CSV files.
- **Web Dashboard:** UI to view live feeds, session summaries, and captured evidence.

## 🛠️ Tech Stack
- **Backend:** Python, Flask
- **AI/ML:** TensorFlow, Keras, OpenCV
- **Frontend:** HTML5, Jinja2

## 📂 Project Structure
- `flask_driver_app/`: Core application logic and Flask server.
- `STINK3014_A251_Project/`: Contains deployment code, baseline models, and project documentation.
- `static/snapshots/`: Saved images of detected violations.
- `stress_detector_cnn_improved.h5`: The trained deep learning model.

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
   Open `http://127.0.0.1:5000` in your browser.
