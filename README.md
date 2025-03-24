# Finger-Driven LED Control with Arduino

This project is a hand gesture-based system that controls the state of LEDs using an **Arduino** and a **Python application**. The Python application uses computer vision and hand tracking to detect the number of fingers raised by the user. Based on the finger count, different LEDs on the Arduino are activated to display different colors.

## Features:
- **Hand Tracking**: Uses the `cvzone` and `mediapipe` libraries for detecting the number of fingers raised.
- **LED Control**: Based on the number of fingers raised, LEDs connected to the Arduino blink in different colors:
  - 1 finger = Green LED 🌱
  - 2 fingers = Red LED 🔴
  - 3+ fingers = Combination of LED effects 🌈

## Requirements:

### Software:
- **Python 3.x** 
- Libraries: 
  - `cvzone`
  - `mediapipe`
  - `pyfirmata`

You can install the required libraries using:
```bash
pip install cvzone mediapipe pyfirmata
Hardware:
Arduino UNO or similar

5 LEDs

Resistors (Typically 220Ω for each LED)

Breadboard (for easy connections)

Jumper wires

Webcam for hand tracking

Setup Instructions:
1. Wiring the LEDs to the Arduino:
Connect each of the 5 LEDs to the Arduino as follows:

LED 1 (Green): Connect the anode (long leg) to pin 8 of Arduino, cathode (short leg) to ground (GND).

LED 2 (Red): Connect the anode to pin 9 of Arduino, cathode to ground (GND).

LED 3 (Blue): Connect the anode to pin 10 of Arduino, cathode to ground (GND).

LED 4 (Yellow): Connect the anode to pin 11 of Arduino, cathode to ground (GND).

LED 5 (White): Connect the anode to pin 12 of Arduino, cathode to ground (GND).

Use 220Ω resistors to limit current going through the LEDs to prevent burning them out.

2. Upload Arduino Code:
Open the Arduino IDE and connect your Arduino to your PC.

In the controller.py file, you'll find the code for controlling the LEDs. This script will use pyFirmata to communicate with the Arduino.

Upload a compatible sketch from the controller.py file to your Arduino to control the LEDs based on the Python script's commands.

3. Running the Python Script:
Clone this repository to your local machine.

Make sure all required libraries (cvzone, mediapipe, pyfirmata) are installed.

Run the Python script (main.py):

bash
Copy
python main.py
The system will now use your webcam to track hand gestures. Based on the number of fingers raised, different LEDs on the Arduino will blink accordingly:

1 finger = Green LED 🌱

2 fingers = Red LED 🔴

3+ fingers = Combination of LED effects 🌈

4. Test the System:
Raise your fingers in front of the webcam. The system should recognize the number of fingers raised and control the LEDs accordingly.

How it works:
The Python script continuously captures frames from the webcam.

It uses hand tracking to count the number of raised fingers using the cvzone and mediapipe libraries.

Based on the finger count, different LEDs on the Arduino blink in different patterns (Green, Red, or other combinations).

License:
This project is licensed under the MIT License - see the LICENSE file for details.
