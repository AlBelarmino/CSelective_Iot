#Laboratory Activity #1: Arduino LED Sequence

##Objective:
The goal of this project is to develop a sequential LED control system where LEDs illuminate and turn off in a predetermined order. The system can be adjusted to operate either odd or even-numbered LEDs separately.

##Description:
This project demonstrates how multiple LEDs connected to an Arduino can be controlled in a sequential pattern with a delay between each activation. Users will observe the LEDs lighting up one after another, followed by turning off in the same order.
LED Pins (ledPins[]): An array storing the pins connected to the LEDs.
Number of LEDs (numLeds): Represents the total count of LEDs used.
Setup: Configures each LED pin as an output.
Loop: Manages the sequence in which LEDs turn on and off.
Instructions:
Wiring the LEDs: Connect the LEDs to the designated pins on the microcontroller.
Uploading the Code: Transfer the provided program to the microcontroller.
Executing the Code: The LEDs will sequentially turn on and off with a delay of one second.
Modifying for Odd/Even Control:
To control odd-numbered LEDs, modify the loop function to activate only the LEDs at odd indices.
To control even-numbered LEDs, adjust the loop function to activate only the LEDs at even indices.
