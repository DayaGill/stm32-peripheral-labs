# Lab 03 — I2C + LCD + AHT20 Sensor + Moving Average

## Goal
Use I2C to communicate with peripherals and display live data:
- Display values on an LCD over I2C
- Read temperature from an AHT20 sensor (I2C address 0x38)
- Apply a moving average filter to stabilize readings

## What I Implemented
- Float formatting: converted a float into integer whole + fractional digits for clean LCD display
- Generated a sine wave signal and displayed step count + formatted values on the LCD
- AHT20 temperature reading over I2C and displayed last readings + current reading
- Moving average filter (size 16) to smooth temperature readings before display

## Key Concepts
- I2C pull-up resistor sizing (rise time / RC constant)
- Reliability improvements via oversampling and averaging
- Addressing options for multiple devices on the same I2C bus
- Level shifting (bi-directional MOSFET-based I2C level shifter concept)

## Evidence / Results
- LCD displays step count and values updating each second
- Temperature read/display workflow with previous values and current in brackets
- Filtered average temperature displayed after moving average

## Notes
This lab is based on my Lab 3 report for ECE 4240.

