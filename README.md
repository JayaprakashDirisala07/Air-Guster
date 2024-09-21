
Hand Gesture Controlled Mouse 🖐️🖱️

Overview
This project enables you to control your computer's mouse cursor using hand gestures, detected through a webcam. Leveraging computer vision techniques, hand movements and gestures are translated into mouse actions such as moving the cursor and clicking.

Key Components
OpenCV

Used to capture video from the webcam.
Provides tools for image processing and manipulation.
MediaPipe

A framework developed by Google for building multimodal (e.g., video, audio) machine learning pipelines.
Utilized for hand tracking to detect and track hand landmarks in real-time.
PyAutoGUI

A Python library for programmatically controlling the mouse and keyboard.
Moves the mouse cursor and performs click actions based on hand gestures.
Process Flow
Video Capture

The webcam continuously captures video frames.
Each frame is processed to detect hand landmarks.
Hand Detection and Tracking

MediaPipe’s hand tracking model identifies key hand landmarks such as finger tips and the palm base.
The model provides normalized coordinates (values between 0 and 1) for these landmarks.
Coordinate Conversion

The normalized hand landmarks are converted into pixel coordinates based on screen dimensions.
This allows hand movements to map to corresponding positions on the screen.
Mouse Control

The index finger tip position is used to move the mouse cursor.
The distance between the index finger tip and thumb tip is used to detect a "click" gesture.
If this distance falls below a certain threshold, a mouse click is performed.
Click Delay Management

A delay is introduced between consecutive clicks to avoid unintended multiple clicks.
This ensures clicks are only registered when sufficient time has passed.
Practical Applications
Accessibility: Provides an alternative input method for individuals with physical disabilities.
Touchless Interfaces: Useful in environments where touchless interaction is preferred, such as in medical settings or public kiosks.
Interactive Installations: Can be used in interactive art installations or exhibitions to create engaging user experiences.
Challenges and Considerations
Lighting Conditions: Hand detection accuracy may vary based on lighting conditions.
Background Noise: A cluttered background can interfere with hand tracking.
Gesture Sensitivity: The system’s gesture sensitivity needs to be fine-tuned to avoid false positives while maintaining responsiveness.

-------------------------------------------------------------------------------------------------------------------

Installation
To set up the project, follow these steps:

-------------------------------------------------------------------------------------------------------------------
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/hand-gesture-controlled-mouse.git
cd hand-gesture-controlled-mouse
-------------------------------------------------------------------------------------------------------------------
Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
-------------------------------------------------------------------------------------------------------------------

Run the application:
bash
Copy code
python hand_gesture_mouse.py
Requirements
Python 3.x
OpenCV
MediaPipe
PyAutoGUI'
-------------------------------------------------------------------------------------------------------------------
Example of Use
Once the script is running, you can control the mouse by moving your hand in front of the webcam. Pinching your index finger and thumb together simulates a mouse click.
-------------------------------------------------------------------------------------------------------------------
Contributing
Contributions are welcome! If you have ideas or improvements, feel free to open an issue or submit a pull request.
-------------------------------------------------------------------------------------------------------------------
License
This project is licensed under the MIT License - see the LICENSE file for details.
-------------------------------------------------------------------------------------------------------------------
Acknowledgements
OpenCV
MediaPipe
PyAutoGUI
Feel free to customize the links, project name, and add any additional details specific to your implementation.
-------------------------------------------------------------------------------------------------------------------
