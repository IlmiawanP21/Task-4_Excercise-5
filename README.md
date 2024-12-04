# FreeRTOS LED Blinking Example on STM32

This repository contains an example program to demonstrate the use of FreeRTOS on STM32 for controlling LED blinking using two separate tasks: one for a green LED and another for a red LED. The program runs two tasks concurrently, simulating multitasking on the STM32 microcontroller.

## Description

This project demonstrates how to use FreeRTOS for multitasking on an STM32 microcontroller. Two tasks are created to blink the green and red LEDs connected to the STM32 GPIO pins. The green and red LEDs blink at different intervals, showcasing task concurrency.

## Key Features

- **FreeRTOS Tasks**: Two tasks, `GreenLedTask` and `RedLedTask`, are implemented to blink LEDs.
- **Shared Resource Access**: A flag (`startFlag`) is used to demonstrate access to shared resources between tasks.
- **GPIO Configuration**: GPIO pins are configured to control the LEDs.
- **Multitasking**: FreeRTOS scheduler manages the two tasks to run concurrently.

## LED Blinking Behavior

- **Green LED**: Flashes every 500ms.
- **Red LED**: Flashes every 100ms.

## Hardware Setup

- **Green LED**: Connected to GPIOA_PIN_0.
- **Red LED**: Connected to GPIOA_PIN_2.
- **Blue LED**: Connected to GPIOA_PIN_1 (not used in this example, but available for future tasks).

## Files

- `main.c`: Main program containing initialization, FreeRTOS tasks, and GPIO configurations.
- `cmsis_os.h`: FreeRTOS API header for STM32.
- `stm32f4xx_hal.h`: STM32 HAL header for hardware abstraction.

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/IlmiawanP21/Task-4_Excercise-5
