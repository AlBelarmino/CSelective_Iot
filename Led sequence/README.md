# Laboratory Activity #1: Arduino Circuit

## Objective:
- The objective of this project is to create a sequential LED lighting system where LEDs turn on and off in a specific order. The system follows a running light effect by lighting up each LED one after another.

## Description:
This activity controls multiple LEDs connected to an Arduino, turning them on and off sequentially with a delay between each action. The system allows users to observe LEDs being lit one by one, followed by turning them off in the same sequence.

- **LED Pins (`ledPins[]`)**: An array of pins to which the LEDs are connected.
- **Number of LEDs (`numLeds`)**: The total number of LEDs in the array.
- **Setup**: Initializes each LED pin as an output.
- **Loop**: Controls the sequence in which LEDs turn on and off.

## Instructions:

1. **Connect the LEDs**: Attach LEDs to the specified digital pins on the microcontroller (e.g., pins 12, 11, 10, 9, and 8).
2. **Upload the Code**: Load the provided Arduino sketch onto your microcontroller.
3. **Run the Code**: The LEDs will sequentially turn on and off with a delay of 1 second between each action.

## Customization:

- **Modify Delay Time**: Adjust the delay time in the loop to speed up or slow down the LED sequence.
- **Reverse Order**: Change the loop direction to make the LEDs turn on from the last pin to the first.
- **Increase Number of LEDs**: Expand the `ledPins[]` array to control more LEDs.
