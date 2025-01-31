## Objective
- This project aims to implement a fire detection system using an Arduino. It utilizes a temperature sensor and a photoresistor to detect high temperatures and brightness levels, triggering an LED warning signal if a fire is detected.

## Description
This system monitors environmental conditions through sensors and activates an LED alarm when both temperature and brightness exceed predefined thresholds.

- **Temperature Sensor (`Temp_Sensor_Pin`)**: Reads temperature values.
- **Photoresistor (`Photo_Sensor_Pin`)**: Detects ambient brightness.
- **LED Indicator (`LED_PIN`)**: Flashes when fire conditions are met.
- **Temperature Threshold (`Tempmax_Treshold`)**: Maximum allowable temperature before fire detection triggers.
- **Brightness Threshold (`Brightnessmax_Treshold`)**: Maximum brightness level before fire detection triggers.
- **Beta Value (`BetaValue`)**: Used for thermistor calculations.
- **Series Resistance (`Series_Resistance`)**: Part of the resistance network for temperature measurement.

## Instructions
1. **Wiring the Sensors**: Connect the temperature sensor, photoresistor, and LED to the designated pins.
2. **Uploading the Code**: Transfer the program to the Arduino board.
3. **Executing the System**: The system will continuously monitor temperature and brightness.
4. **Fire Detection Logic**:
   - The temperature is read using a thermistor and converted to Celsius.
   - Brightness is measured using a photoresistor and categorized as "Bright" or "Dark."
   - If temperature exceeds `50.0°C` and brightness surpasses `220`, the LED blinks three times to indicate fire.
   - Otherwise, the LED remains off.
5. **Modifications**:
   - Adjust the `Tempmax_Treshold` and `Brightnessmax_Treshold` values for different sensitivity levels.
   - Change the LED blinking pattern for different alert signals.
