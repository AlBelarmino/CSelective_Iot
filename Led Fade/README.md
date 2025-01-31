## Objective
- This project aims to implement a fading LED sequence where LEDs gradually brighten to a target intensity before turning off. The system follows a sequential pattern with controlled brightness levels.

## Description
This project demonstrates how multiple LEDs connected to an Arduino can be gradually brightened and then turned off using Pulse Width Modulation (PWM). The brightness increases gradually until a defined limit before transitioning to the next LED.

- **LED Pins (`ledPins[]`)**: An array storing the pins connected to the LEDs.
- **Number of LEDs (`numLeds`)**: Represents the total count of LEDs used.
- **Setup**: Configures each LED pin as an output.
- **Loop**: Calls functions to sequentially brighten and then turn off LEDs.
- **`LedON()` Function**: Gradually increases the brightness of each LED to a mapped value.
- **`LedOFF()` Function**: Turns off all LEDs sequentially.

## Instructions
1. **Wiring the LEDs**: Connect the LEDs to the specified pins on the microcontroller.
2. **Uploading the Code**: Transfer the provided program to the microcontroller.
3. **Executing the Code**: The LEDs will gradually brighten to a set brightness and then turn off in sequence.
4. **Understanding Brightness Mapping**:
   - The brightness of each LED is mapped between `150` and `2700`.
   - The brightness is increased incrementally to reach the target intensity.
5. **Modifications**:
   - Adjust the brightness mapping values for different lighting effects.
   - Modify the delay durations for different fading speeds.
