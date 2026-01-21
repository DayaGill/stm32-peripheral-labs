# Lab 01 — GPIO + Rotary Encoder (STM32F407)

## Goal
Get comfortable with the STM32F407 Discovery board and basic I/O:
- Blink onboard LED using HAL GPIO
- Measure rotary encoder signals with a logic analyzer
- Decode rotation direction and change LED output accordingly

## What I Implemented
- GPIO output control to blink LED3 using `HAL_GPIO_WritePin` + `HAL_Delay`
- Captured encoder waveforms and observed Gray code patterns using a Saleae Logic Analyzer
- Wrote rotary encoder state-tracking logic to detect CW/CCW direction and toggle LEDs

## Key Concepts
- GPIO configuration and pin control
- Switch bounce (and why encoder outputs can look “glitchy”)
- Debouncing strategies (RC hardware debounce and sampling-based software debounce)

## Evidence / Results
- Logic analyzer capture of clockwise waveform
- Direction detected by reading previous/current encoder states and updating a LED counter

## Notes
This lab is based on my Lab 1 report for ECE 4240.

