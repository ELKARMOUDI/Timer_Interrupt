# STM32F411 Nucleo Timer Interrupt Example

![STM32F411](https://img.shields.io/badge/STM32F411-Nucleo-blue)
![TIM10](https://img.shields.io/badge/TIM10-Interrupt-green)

<img src="https://github.com/user-attachments/assets/4c574b08-8542-4e3d-8ace-b6607aaccf0d" width="50%" alt="Description">



Toggle LED at 1Hz using TIM10 interrupts on STM32F411 Nucleo.

## Features
- **Precise 1Hz Timing** via TIM10 interrupts
- **Interrupt-Driven** - No `HAL_Delay()` usage
- **Onboard LED** control (PA5)
- **16MHz HSI Clock** (No PLL required)

## Hardware Configuration
| Component | Specification | Nucleo Reference |
|-----------|---------------|------------------|
| MCU       | STM32F411RE   | MB1136 User Manual |
| LED       | PA5           | CN10 pin 21 |
| Clock     | HSI 16MHz     | Internal |

## Technical Details
### Clock Configuration 
```c
HSI (16MHz) → SYSCLK
APB2 Prescaler = 1 → TIM10 Clock = 16MHz
