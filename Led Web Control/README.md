## Objective
- This project enables remote control of an LED connected to an Arduino using FastAPI. The LED can be turned on or off through HTTP requests sent to the FastAPI server, which communicates with the Arduino over a serial connection.

## Description
This system integrates an Arduino and a Python-based FastAPI server to control an LED remotely. The Arduino listens for serial commands (`'1'` to turn on, `'0'` to turn off), while the FastAPI server provides an API for sending these commands.

- **Arduino Setup:** The Arduino reads serial input and controls an LED on pin 13.
- **FastAPI Server:** Provides endpoints (`/led/on`, `/led/off`) to send commands to the Arduino.
- **Serial Communication:** Establishes a connection between the Arduino and the FastAPI server over a specified COM port.

## Instructions

### 1. Setting Up the Arduino
- Connect an LED to pin 13.
- Upload the provided Arduino sketch to the board.

### 2. Setting Up the FastAPI Server
- Ensure Python and FastAPI are installed (`pip install fastapi serial`).
- Run the Python script to start the server (`fastapi dev &lt;name_of_file&gt;.py`).

### 3. Controlling the LED
- Send a POST request to `http://127.0.0.1:8000/led/on` to turn on the LED.
- Send a POST request to `http://127.0.0.1:8000/led/off` to turn off the LED.
- The server communicates with the Arduino via the serial port (`COM3` by default).

## Functions Explained

### Arduino Code
- **`setup()`**: Initializes the serial connection and sets pin 13 as an output.
- **`loop()`**: Listens for serial input and toggles the LED accordingly.

### FastAPI Code
- **`startup_event()`**: Establishes a serial connection to the Arduino.
- **`shutdown_event()`**: Closes the serial connection when the server stops.
- **`turn_led_on()`**: Sends `'1'` to the Arduino via serial to turn on the LED.
- **`turn_led_off()`**: Sends `'0'` to the Arduino via serial to turn off the LED.

## Modifications & Enhancements
- Change the COM port if needed (`arduino = serial.Serial('COM3', 9600, timeout=1)`).
- Add more API endpoints for additional Arduino controls.
- Implement a web interface to trigger API requests easily.
