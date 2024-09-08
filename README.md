# **Women Safety Analytics using ML (DeepFace)**

## **Project Overview**
This project is designed to enhance women's safety using advanced Machine Learning (ML) models for gender bias detection. It integrates **facial recognition**, **gesture recognition**, and **audio analysis** to monitor environments in real-time and proactively alert in cases of potential danger or abnormal gender ratios. By analyzing video feeds frame-by-frame and detecting certain gestures like SOS signals, this system aims to provide early warnings and help prevent unsafe situations.

---

## **Features**

- **Real-Time Gender Bias Detection**: Analyze video and audio streams to identify gender imbalances in a scene, particularly in sensitive environments.
  
- **Gesture Recognition for SOS Alerts**: Detect SOS or similar distress gestures using hand gesture recognition powered by MediaPipe.
  
- **Proactive Alerting**: Alerts are triggered based on scenarios such as a high male-to-female ratio, sudden increases in male presence, or large group gatherings.

- **Voice and Gesture Integration**: The system integrates multiple modalities (voice, face, gestures) for a comprehensive safety solution.

- **Privacy-Focused AI**: Built with privacy and ethical considerations, this solution processes data securely without retaining unnecessary information.

---

## **Project Structure**

```bash
├── models/                     # Contains ML models for face and gender detection
├── src/
│   ├── video_analysis.py        # Video processing logic, breaking video into frames for analysis
│   ├── gender_bias_detection.py # DeepFace-based gender bias detection
│   ├── gesture_detection.py     # Gesture detection using MediaPipe
│   └── audio_analysis.py        # (Optional) Audio processing for speech recognition
├── data/                        # (Optional) Placeholder for sample videos or images
├── requirements.txt             # Python dependencies
└── README.md                    # Project documentation
```

---

## **Key Components**

### **Video Analysis**
This component processes video feeds or webcam streams, breaking them into frames to detect the number of men and women using DeepFace.

### **Gender Bias Detection**
Using **DeepFace**, the system determines the gender of individuals in the frame and compares gender ratios. If suspicious patterns (e.g., a 4:1 male-to-female ratio) are detected, an alert is generated.

### **Gesture Detection**
Powered by **MediaPipe**, the system analyzes hand gestures to detect SOS or distress gestures. If an SOS gesture is detected, the system sends a real-time alert.

---

## **Alerts**

Alerts are generated based on predefined suspicious activity scenarios:

- **High male-to-female ratio** (e.g., 4:1 or higher)
- **Large group gatherings** (more than 10 people in the frame)
- **Sudden changes in gender counts**
- **SOS gestures** detected via hand movements

---

## **Setup Instructions**

### **Prerequisites**

- Python 3.7 or above
- OpenCV
- MediaPipe
- DeepFace
- NumPy
- (Optional) Google Colab for cloud-based execution

---


```bash
pip install -r requirements.txt
```

### **Running the Program**:

#### **Webcam-based Detection**:
```bash
python src/webcam_analysis.py
```

#### **Video-based Detection**:
Update the video path in the script and run:
```bash
python src/video_analysis.py --video /path/to/video.mp4
```

---

## **How It Works**

- **Gender Detection**: The DeepFace model analyzes each frame of the video or live feed to detect the gender of each person in the frame. If the male-to-female ratio becomes imbalanced (e.g., 4 men to 1 woman), an alert is triggered.

- **Gesture Recognition**: Using MediaPipe, the system monitors hand gestures in real-time. If an SOS gesture (or similar) is detected, it flags the frame as suspicious.

- **Alerting Mechanism**: Alerts are triggered when predefined conditions (e.g., large groups, high male-to-female ratios, SOS gestures) are detected.

---

## **Scenarios Detected**

- **High Male-to-Female Ratio**: Triggered when the male population in a frame is disproportionately higher than the female population.
- **Large Groups**: Detects gatherings of more than 10 people in a frame.
- **SOS Gesture**: Detects distress signals through hand gestures using MediaPipe.
- **Sudden Changes in Gender Count**: Flags frames where the count of men or women changes drastically from one frame to another.

---

## **Customization**

You can customize the alert scenarios in `gender_bias_detection.py` and `gesture_detection.py` by adjusting the parameters for ratios, group sizes, or specific gesture conditions.

---

## **Future Enhancements**

- **Audio Analysis**: Integrate speech recognition and voice tone analysis to detect distress calls.
- **Mobile App Integration**: Provide alerts through a mobile app for immediate notifications.
- **Crowd Density Monitoring**: Enhance the system to analyze crowd density in large spaces.

---

## **Contributing**

Feel free to contribute to this project by opening a pull request or raising an issue on GitHub. We welcome suggestions for new features, optimizations, or bug fixes.

---

## **License**

This project is licensed under the MIT License. See the LICENSE file for more details.

---


