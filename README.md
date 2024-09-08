Gender Bias Detection and Gesture Recognition
This project integrates multiple machine learning models to detect gender bias and recognize gestures in real-time video streams using a webcam. The system can analyze both face data (for gender bias) and hand gestures, and can be extended to include audio analysis for comprehensive monitoring.

Features
Gender Bias Detection: Uses DeepFace to detect and analyze the gender of individuals in video frames or images. The system flags any significant gender bias, such as a disproportionate number of men compared to women.
Gesture Recognition: Detects SOS hand gestures using MediaPipe, primarily used for emergency detection.
Real-Time Analysis: Leverages webcam input for real-time frame-by-frame analysis, combining both gender detection and gesture recognition.
Extensibility: Includes optional audio analysis for speech recognition and action triggers.
Requirements
Python 3.x
TensorFlow
OpenCV
MediaPipe
DeepFace
Numpy


Usage
Gender Bias Detection:

This component analyzes frames from a webcam feed to detect gender bias. The results are printed, showing the number of men and women in each frame. Alerts are triggered if certain thresholds are reached.
Gesture Detection:

This system detects specific SOS gestures in the video feed. If the gesture is detected, the system triggers a real-time alert.

Customization
Gender Bias Thresholds: The gender bias detection can be customized to trigger alerts based on different gender ratios or counts.
Gesture Detection Logic: Modify the gesture detection code in gesture_detection.py to add or change gestures recognized by the system.
Contribution
Feel free to fork this project and submit pull requests for improvements or bug fixes.

License
This project is licensed under the MIT License.
