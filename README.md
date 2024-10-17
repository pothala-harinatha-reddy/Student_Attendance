# Student_Attendance_System
Face Recognition

This is a simple Student Attendance System that detects and matches faces from a group image with a predefined dataset of student names and USNs. The system captures detected face data and stores it in an SQLite database, which can later be used to track attendance.

# Features
  - Face detection using Haar Cascade Classifier.
  - Matches detected faces with a dataset of student names and USNs.
  - Annotates the group image with detected faces, names, and USNs.
  - Stores the attendance information (name and USN) in an SQLite database.

# Prerequisites
  Before running the project, ensure you have the following installed:
  
  - Python 3.x
  - OpenCV
  - SQLite3
  - Numpy
    
  You can install the required packages using pip:
  ## pip install opencv-python numpy

# Dataset Format
  The dataset is loaded from a CSV file containing student information. The CSV should follow this structure:
  
  id,name,usn,photo_url
  1,John Doe,USN12345,https://example.com/john_doe.jpg
  2,Jane Smith,USN67890,https://example.com/jane_smith.jpg
  ...
  The system reads the CSV file, extracts the student names and USNs, and uses this information to match detected faces in the group picture.

# Project Structure
  - **faces.db:** SQLite database to store attendance information.
  - **face_data.csv:** CSV file containing student names, USNs, and photo URLs.
 - **P21.png:** Group image file where the system will detect and annotate faces.
  - **haarcascade_frontalface_default.xml:** Haar Cascade Classifier XML file for face detection.
# How It Works
  - **Face Detection:** The system uses OpenCV’s Haar Cascade Classifier to detect faces in the group image.
  - **Matching Faces with Dataset:** For each detected face, it attempts to match the face with student records in the dataset.
  - **Attendance Tracking:** If a match is found, the student's name and USN are annotated on the image, and the data is saved to the SQLite database.
  - **Image Display:** The group image is displayed with the detected faces, names, and USNs.
# Usage
  - Place your group image (e.g., P21.png) in the project directory.
  - Modify the face_data.csv file to include your dataset.
 **Run the script:**
  - python attendance_system.py
  - The program will detect faces in the group image, match them with the dataset, and display the annotated image. Attendance data will be saved in the faces.db SQLite database.
