## Objective
- This project enables remote control of an LED using a button connected to an Arduino, with API integration through FastAPI. The system detects button presses and triggers LED control via HTTP requests.

## Description
This system integrates an Arduino, a button, and a Python-based FastAPI server for LED control. The Arduino detects button presses and sends signals to the FastAPI server, which processes the input and triggers the LED accordingly.

- **Arduino Setup:** Reads button input from pin 12 and sends signals via serial communication.
- **FastAPI Server:** Provides endpoints (`/led/on`, `/led/off`) to control the LED.
- **Serial Communication:** Establishes a connection between the Arduino and the FastAPI server over a specified COM port.

## Instructions

### 1. Setting Up the Arduino
- Connect a button to pin 12 with a pull-down resistor.
- Upload the provided Arduino sketch to the board.

### 2. Setting Up the FastAPI Server
- Ensure Python and FastAPI are installed (`pip install fastapi serial requests`).
- Run the Python script to start the server (`uvicorn script_name:app --reload`).

### 3. Controlling the LED
- The Arduino reads button input and sends `1` (pressed) or `0` (not pressed) via serial.
- The FastAPI server interprets this data and calls the API to control the LED.
- The server sends a request to `http://127.0.0.1:8000/led/on` when the button is pressed.
- The server sends a request to `http://127.0.0.1:8000/led/off` when the button is released.

## Functions Explained

### Arduino Code
- **`setup()`**: Initializes serial communication and button input.
- **`loop()`**: Reads the button state and sends `1` or `0` via serial.

### FastAPI Code
- **`startup_event()`**: Establishes a serial connection to the Arduino.
- **`shutdown_event()`**: Closes the serial connection when the server stops.
- **`read_serial_data()`**: Reads button states from the Arduino and calls the appropriate API endpoint.
- **`turn_led_on()`**: Sends a request to turn on the LED when the button is pressed.
- **`turn_led_off()`**: Sends a request to turn off the LED when the button is released.

## Modifications & Enhancements
- Change the COM port if needed (`arduino = serial.Serial('COM3', 9600, timeout=1)`).
- Adjust debounce timing in the Arduino code to avoid false triggers.
- Implement a web interface for monitoring button presses and LED status.
