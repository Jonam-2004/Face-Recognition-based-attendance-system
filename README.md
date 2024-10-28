# Face Recognition Based Attendance System

This project is a Face Recognition-based Attendance System using OpenCV and Flask. It enables automated attendance tracking by identifying faces and logging entry and exit times. The system captures images, recognizes faces in real-time, and stores attendance records for further analysis. 

## Features
- **Face Detection and Recognition**: Detects and identifies registered faces using OpenCV.
- **Attendance Logging**: Automatically logs attendance by recording entry and exit times, as well as the duration of presence.
- **Interactive UI**: Web-based interface built with Flask to view attendance records and manage users.
- **Real-time Attendance**: Uses live camera feed for face recognition and attendance tracking.

## Folder Structure
- `Attendance/` - Stores daily attendance records in CSV format.
- `static/faces/` - Stores individual face images for each registered user.
- `static/face_recognition_model.pkl` - Contains the trained face recognition model.

## Requirements
- Python 3.x
- Flask
- OpenCV
- NumPy
- pandas
- scikit-learn
- joblib

## Installation
1. Clone the repository.
   ```bash
   git clone https://github.com/yourusername/face-recognition-attendance.git
   cd face-recognition-attendance
2.Install the required packages.
   ```bash
   pip install -r requirements.txt
3.Make sure to download and add the haarcascade_frontalface_default.xml file to your project directory for face detection.
