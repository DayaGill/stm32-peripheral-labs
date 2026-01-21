# Lab 05 — SPI LCD + DMA Benchmark + Pong (ADC + EWMA)

## Goal
Use SPI peripherals and DMA to drive an LCD efficiently:
1) Bring up ST7735 LCD and display test patterns/images
2) Benchmark drawing operations without DMA vs with DMA
3) Build a Pong-style game controlled by a potentiometer (ADC + filtering)

## What I Implemented
- LCD bring-up:
  - configured SPI and connected ST7735 per pinout
  - displayed text in different sizes/colors and images
- DMA benchmarking:
  - measured average execution time for many drawing ops
  - enabled DMA SPI mode and compared results
  - observed large overall speedup (73x overall)
- Pong game:
  - read potentiometer via ADC
  - oversampled ADC (16x) and applied EWMA filter to smooth paddle control
  - ran the Pong game loop using filtered input

## Key Concepts
- Why DMA improves throughput for repeated transfers to LCD
- Double buffering concept in the LCD driver workflow
- Effect of EWMA alpha on responsiveness vs smoothness
- Estimating FPS based on screen transfer time (≈65.8 FPS in this setup)

## Evidence / Results
- LCD photos (text, image, benchmark output screen)
- Non-DMA vs DMA benchmark times displayed
- Pong screenshots and “Game Over” screen

## Notes
This lab is based on my Lab 5 report for ECE 4240.

