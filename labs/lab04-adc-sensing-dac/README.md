# Lab 04 — ADC Sensing + Temperature Control + PWM “Bad DAC”

## Goal
Work with ADC sampling, sensors, filtering, and basic control behavior:
1) Read STM32 internal temperature sensor using ADC1, moving average, and console output
2) Read external TMP36 sensor using ADC2 with oversampling + moving average
   - set a desired temperature via potentiometer
   - implement hysteresis to prevent flicker
3) Approximate a DAC using PWM + RC low-pass filter and verify on oscilloscope

## What I Implemented
- Internal temp sensing:
  - sampled ADC1 8 times/sec
  - moving average (8 samples)
  - calibrated conversion to °C and printed once/sec
- External temp sensing (TMP36):
  - oversampled sensor readings (8x at 8 Hz)
  - oversampled potentiometer readings (16x at 4 Hz)
  - scaled setpoint and implemented hysteresis (2°C band)
- PWM “DAC”:
  - used PWM + RC filter (~1.06 kHz cutoff using 1.5kΩ and 0.1µF)
  - oversampled output (64x) and plotted ADC avg vs duty cycle
  - verified waveform on oscilloscope

## Key Concepts
- Oversampling and moving average filtering
- Hysteresis control loop (prevents rapid toggling near threshold)
- PWM-to-analog approximation using low-pass filtering

## Evidence / Results
- Console temperature output (internal sensor)
- LED control based on hysteresis around setpoint
- Oscilloscope verification + linear ADC vs duty behavior

## Notes
This lab is based on my Lab 4 report for ECE 4240.

