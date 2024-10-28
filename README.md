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
1.**Clone the repository.**
  bash
      git clone https://github.com/yourusername/face-recognition-attendance.git
      cd face-recognition-attendance

2.**Install the required packages.**
  bash
  pip install -r requirements.txt
3.Make sure to download and add the haarcascade_frontalface_default.xml file to your project directory for face detection.

## Usage
Start the Server
bash
python app.py
The app will run on http://127.0.0.1:5000/ by default.

## Adding a New User:

-Navigate to /add in the app.
-Provide a unique username and ID.
-The camera will capture images for training the model. Make sure the user’s face is clear during image capture.

## Start Attendance:
-Navigate to /start.
-The camera will begin capturing frames and detecting faces.
-Recognized faces will be marked in the attendance record with entry and exit times.

## View Attendance Records:

Attendance data is stored as a CSV file in the Attendance/ folder.
You can also view the records directly in the UI.

## Project Workflow
Face Detection: The system uses Haar Cascades for face detection.
Face Recognition: A K-Nearest Neighbors (KNN) model is used to recognize faces. It is trained on captured face images for each user.
Attendance Logging: For each recognized face, the system logs entry and exit times. If the user stays for the required duration, they are marked "Present."


## Code Overview
app.py: Main file containing all the routes and core logic for the application.
train_model(): Function to train the KNN model using the captured face images.
extract_faces(): Detects faces in an image using Haar Cascades.
add_attendance(): Logs the attendance of identified individuals, including entry and exit times.


## Example Data
Sample attendance records are stored in CSV format in the Attendance/ folder. Each entry includes:

Name: Name of the recognized individual.
Roll: Unique ID.
Entry Time: The time when the individual is first recognized.
Exit Time: The time when the individual is last recognized.
Present Hours: The total time in minutes between entry and exit.
Status: Attendance status based on duration ("Present," "Absent," or "Notable").


## Dependencies
The project uses the following libraries:

OpenCV: For face detection and real-time video capture.
Flask: For creating the web-based interface.
NumPy: For numerical operations on image data.
pandas: For handling CSV files.
scikit-learn: For KNN-based face recognition.
joblib: For saving and loading the trained model.


## Future Improvements
Implement a more robust face recognition model (e.g., deep learning-based).
Add more sophisticated attendance status tracking.
Integrate with a database for persistent storage.

## License
This project is licensed under the MIT License. See the LICENSE file for details.
