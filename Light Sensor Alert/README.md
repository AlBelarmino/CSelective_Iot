## Objective
- This project implements a light intensity monitoring system using an Arduino. It utilizes a photoresistor to measure ambient brightness and an LED to indicate brightness levels. The system can also receive serial input to stop the blinking.

## Description
This system continuously measures ambient brightness and categorizes it as either "Bright" or "Dark." If brightness exceeds a predefined threshold, an LED blinks as an alert.

- **Photoresistor (`PHOTO_SENSOR_PIN`)**: Measures light intensity.
- **LED Indicator (`LED_PIN`)**: Blinks when brightness exceeds a threshold.
- **Brightness Threshold (`BRIGHTNESS_THRESHOLD`)**: The level at which brightness is considered high.
- **Serial Input Handling**: Allows stopping the blinking using a "stop" command.

## Instructions
1. **Wiring the Sensors**: Connect the photoresistor and LED to the designated pins.
2. **Uploading the Code**: Transfer the program to the Arduino board.
3. **Executing the System**:
   - The system continuously monitors brightness and displays its status on the Serial Monitor.
   - If brightness exceeds `22%`, the LED blinks to indicate high brightness.
   - If a "stop" command is received via Serial Monitor, blinking is stopped.
4. **Functions Explained**:
   - `readBrightness()`: Reads and maps the brightness level.
   - `getBrightnessStatus()`: Returns "Bright" or "Dark" based on the threshold.
   - `checkLightCondition()`: Sets the blinking state based on brightness.
   - `handleSerialInput()`: Listens for user input to stop blinking.
5. **Modifications**:
   - Adjust `BRIGHTNESS_THRESHOLD` for different light sensitivity.
   - Change the LED blinking pattern for customized alerts.
