

# Task 02: Timers and Non-Blocking Code

## Project Overview
This project demonstrates non-blocking timing using an
Arduino Uno and two LEDs. It uses millis() to control
two LEDs at different intervals without using delay()
in the main loop.

## Components Required
- Arduino Uno
- 2 LEDs
- 2 resistors (220 ohms)
- Breadboard and jumper wires

## Working
- LED 1 toggles every 1000 milliseconds.
- LED 2 toggles every 500 milliseconds.
- Both timers run independently.
- The main loop does not use delay().

## Why Non-Blocking Code?
The delay() function pauses program execution.
Using millis() allows the Arduino to check multiple
timers while continuing to execute the main loop.

This makes it easier to add sensors and other tasks
without unnecessarily stopping the program.

## How to Run
1. Open the project in Arduino IDE or Wokwi.
2. Connect LED 1 to pin 8 and LED 2 to pin 9,
   each through a current-limiting resistor.
3. Connect both LED negative legs to GND.
4. Upload the code to the Arduino Uno.
5. Observe both LEDs blinking at different rates.

## Timing Method
The project uses millis() polling rather than interrupts.
This is sufficient for independent, non-blocking LED timing.
