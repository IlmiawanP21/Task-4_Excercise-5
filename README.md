# Task-4_Excercise-5 

reeRTOS LED Blinking Example on STM32
This repository contains an example program to demonstrate the use of FreeRTOS on STM32 for controlling LED blinking using two separate tasks: one for a green LED and another for a red LED. The program uses two tasks running concurrently with the help of FreeRTOS to simulate multitasking.

Description
This project demonstrates how to use FreeRTOS for multitasking on an STM32 microcontroller. Two tasks are created to flash LEDs connected to the STM32 GPIO pins. The green LED and red LED blink at different intervals.

Key functionalities:

FreeRTOS Tasks: Two tasks, GreenLedTask and RedLedTask, are implemented to blink LEDs.
Shared Resource Access: A flag (startFlag) is used to demonstrate access to shared resources between the tasks.
GPIO Configuration: GPIO pins are configured to control the LEDs.
Multitasking: FreeRTOS scheduler manages the two tasks to run concurrently.
Features
Green LED: Flashes every 500ms.
Red LED: Flashes every 100ms.
Shared Data Management: A shared flag startFlag is toggled between tasks with synchronization using a simple access function accessSharedData().
System Initialization: The microcontroller system clock is configured, and GPIO pins are initialized for the LEDs.
Files
main.c: Main program containing the initialization, FreeRTOS tasks, and GPIO configurations.
cmsis_os.h: FreeRTOS API header for STM32.
stm32f4xx_hal.h: STM32 HAL header for hardware abstraction.
Hardware Setup
Green LED connected to GPIOA_PIN_0.
Red LED connected to GPIOA_PIN_2.
Blue LED connected to GPIOA_PIN_1 (not used in this example but available for future tasks).
How to Run
Clone the repository:

bash
Salin kode
git clone https://github.com/username/repository.git
Open the project in STM32CubeIDE or STM32CubeMX.

Build and upload the firmware to the STM32 board.

After programming the STM32, you should see the green LED blinking every 500ms and the red LED blinking every 100ms.

Explanation of Key Functions
SystemClock_Config(): Configures the system clock to use the High-Speed Internal (HSI) oscillator.
MX_GPIO_Init(): Initializes the GPIO pins for the LEDs.
GreenLedTask(): Task to control the green LED. It turns on the green LED, calls accessSharedData() to toggle the shared flag, then turns off the green LED and delays for 500ms.
RedLedTask(): Task to control the red LED. It turns on the red LED, calls accessSharedData() to toggle the shared flag, then turns off the red LED and delays for 100ms.
accessSharedData(): Function to simulate access to shared data. It toggles the value of startFlag and controls the state of an additional GPIO pin (not used in the LED flashing logic).
Requirements
STM32 Microcontroller: This example is designed for STM32 boards (e.g., STM32F4 series).
STM32CubeIDE or STM32CubeMX: For building and programming the STM32 firmware.
