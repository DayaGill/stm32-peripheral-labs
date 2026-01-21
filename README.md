# STM32 Peripheral Labs (ECE 4240)

A structured set of embedded systems labs completed on the STM32F407 Discovery board. These labs cover core microcontroller peripherals and practical debugging techniques.

## Highlights
- GPIO + rotary encoder input (with logic analyzer capture)
- Printf debugging over SWV/ITM
- PWM (software + hardware) for LED brightness and motor control
- I2C peripherals: LCD + AHT20 temperature sensor + moving average
- ADC sensing: internal + external temperature sensors, oversampling, hysteresis control
- “Bad DAC” using PWM + RC low-pass filter (verified on oscilloscope)
- SPI LCD driving + performance comparison (DMA vs non-DMA)
- Mini-game (Pong) controlled via ADC + EWMA filtering

## Repo Structure
- `labs/` — each lab has its own README 
- `docs/` — PDFs of lab reports
- `media/` — screenshots/photos (logic analyzer, oscilloscope, LCD output)

## Hardware & Tools
- STM32F407G Discovery board
- Sensors: TMP36, AHT20 (I2C)
- ST7735 LCD (SPI)
- Tools: STM32CubeIDE/HAL, Saleae Logic Analyzer, oscilloscope

## Labs
1. Lab 01 — GPIO + Rotary Encoder
2. Lab 02 — SWV Printf + PWM + Motor Control
3. Lab 03 — I2C + LCD + AHT20 + Moving Average
4. Lab 04 — ADC Sensing + Hysteresis + PWM “DAC”
5. Lab 05 — SPI LCD + DMA Benchmark + Pong (ADC + EWMA)
