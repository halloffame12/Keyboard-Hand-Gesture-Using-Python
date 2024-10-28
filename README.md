# Keyboard-Hand-Gesture-Using-Python
👉 This Python code creates a virtual keyboard that is controlled using hand gestures, allowing users to "type" by moving their hands in front of a camera. The code utilizes the OpenCV library for capturing video input and Mediapipe for hand-tracking, identifying hand landmarks and gestures.

👉 Key Features of the Code:
Hand Detection and Tracking:

1. The code initializes a hand-tracking model (mp.solutions.hands) with dynamic detection and tracking configurations to recognize one hand in the camera feed.
Virtual Keyboard Layout:

2. It creates a 3x10 grid of virtual keys (letters and commands) with customizable layouts for uppercase and lowercase letters.
Button class instances are positioned for each key on the grid, with options like "CL" (Clear), "SP" (Space), and "APR" (Switch Layout) to toggle between uppercase and lowercase layouts.
Gesture-Based Typing:

3. By tracking hand landmarks, the code calculates distances between specific hand points to recognize finger movements, such as pointing or touching a key.
Finger positions and gestures are analyzed to select keys when certain distances are detected.
Display and Visual Feedback:

4. Visual feedback is provided by highlighting keys as the hand hovers over them, allowing the user to see which key is being "pressed."
The typed text appears in a designated area on the screen.
Key Press Simulation:

5. The pynput library is used to simulate keyboard input, allowing typed characters to be recorded on the virtual keyboard.
Distance Calculation for Gesture Accuracy:

6. Polynomial regression is used to calibrate gesture sensitivity, adjusting for hand position changes based on distance.
