# Lab 02 — Printf Debugging + PWM + Motor Control

## Goal
Practice embedded debugging and PWM control:
1) Redirect `printf()` to SWV ITM for fast debugging output
2) Implement software PWM to ramp LED brightness
3) Use hardware PWM to control a vibration motor, adjusting duty cycle via rotary encoder

## What I Implemented
- SWV/ITM `printf` output: prints “ITM printf test #N” with a counter incrementing in the main loop
- Software PWM LED dimming: implemented a microsecond delay using TIM1 and used duty-cycle on/off timing to ramp brightness
- Hardware PWM motor control: configured TIM2 CH1 PWM output and adjusted duty cycle in steps based on rotary encoder direction

## Key Concepts
- Why software PWM doesn’t scale well (interrupts + timing jitter)
- PWM duty cycle vs motor starting behavior (minimum duty threshold)
- Inductive kickback (back-EMF) and protection using a flyback diode

## Evidence / Results
- SWV terminal output showing incrementing printf counter
- LED brightness ramping up/down
- Motor speed changes as duty cycle changes via rotary encoder input

## Notes
This lab is based on my Lab 2 report for ECE 4240.

