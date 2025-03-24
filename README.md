# Finger-Driven LED Control with Arduino

This project is a hand gesture-based system that controls the state of LEDs using an Arduino and a Python application. The Python application uses computer vision and hand tracking to detect the number of fingers raised by the user. Based on the finger count, different LEDs on the Arduino are activated to display different colors.

## Features:
- **Hand Tracking**: Uses the `cvzone` and `mediapipe` libraries for detecting the number of fingers raised.
- **LED Control**: Based on the number of fingers raised, LEDs connected to the Arduino blink in different colors.
  - 1 finger = Green LED
  - 2 fingers = Red LED
  - 3+ fingers = Combination of LED effects

## Requirements:
- Python 3.x
- Libraries: 
  - `cvzone`
  - `mediapipe`
  - `pyfirmata`
  
- Hardware:
  - Arduino UNO or similar
  - 5 LEDs connected to the Arduino
  - A webcam for hand tracking
  
## Setup Instructions:
1. Install the required Python libraries:
   ```bash
   pip install cvzone mediapipe pyfirmata
Connect your Arduino to your PC and upload a compatible sketch to interface with the LEDs.

Run the main.py script in Python to start hand gesture recognition and control the LEDs based on finger count.

How it works:
The Python script continuously captures frames from the webcam.

It uses hand tracking to count the number of raised fingers.

Based on the finger count, different LEDs on the Arduino blink in different patterns (Green, Red, or other combinations).

Project Setup:
Clone this repository to your local machine.

Connect your Arduino and upload the necessary code (found in the controller.py file).

Run the Python script (main.py) to see the system in action.

License:
This project is licensed under the MIT License - see the LICENSE file for details.

Contributing:
Feel free to fork this project, open issues, or submit pull requests. Contributions are always welcome!
