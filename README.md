🧘 Surya Asana Detection using MediaPipe & OpenCV

This project detects Surya Asana (Sun Salutation – basic arm posture) in real time using a webcam.
It uses MediaPipe Pose to track body landmarks and angle calculation to determine whether the arms are in the correct position.

📌 Features

Real-time pose detection using webcam

Uses MediaPipe Pose landmarks

Calculates elbow joint angles

Displays:

✅ Surya Asana Detected!

❌ Not Surya Asana

Visualizes pose skeleton on the screen

🛠️ Technologies Used

Python

OpenCV

MediaPipe

NumPy

📂 Project Structure
surya-asana-detection/
│
├── surya_asana.py        # Main Python file
├── README.md             # Project documentation

⚙️ Requirements

Make sure you have Python 3.7+ installed.

Install the required libraries:

pip install opencv-python mediapipe numpy

▶️ How to Run

Clone the repository:

git clone https://github.com/your-username/surya-asana-detection.git


Navigate to the project folder:

cd surya-asana-detection


Run the script:

python surya_asana.py


Press q to quit the application.

🧠 How It Works

Captures video input from the webcam

MediaPipe detects pose landmarks

Key landmarks used:

Shoulder

Elbow

Wrist

Calculates the elbow angle using vector mathematics

Detection logic:

If both elbow angles are greater than 160°, arms are considered straight

Displays Surya Asana Detected

📐 Angle Calculation Logic

The angle is calculated using three points:

Shoulder → Elbow → Wrist

Using the formula:

cos(θ) = (BA · BC) / (|BA| |BC|)

🧪 Detection Condition (Current)
if left_elbow_angle > 160 and right_elbow_angle > 160:
    Surya Asana Detected


⚠️ Thresholds can be adjusted for better accuracy.

🚀 Future Improvements

Detect all 12 steps of Surya Namaskar

Add voice feedback

Count repetitions

Disease-specific yoga recommendations

Integrate with Django Web App

Store data using SQL database

📸 Sample Output

Pose landmarks drawn on body

Status text displayed on screen

🙌 Acknowledgements

MediaPipe by Google

OpenCV Community

👤 Author

Prasanna Chaganti
B.Tech Graduate | AI & Web Development Enthusiast
