# I2C Scanner for STM32 Microcontrollers

This project provides an **I2C (Inter-Integrated Circuit) bus scanner** designed for STM32 microcontrollers. An I2C scanner is an essential tool for embedded systems development, allowing you to discover and identify I2C devices connected to your microcontroller's I2C bus by **systematically probing all possible I2C addresses**.

---

## What is I2C?

I2C is a widely used **two-wire serial communication protocol** that enables a master device (like an STM32 microcontroller) to communicate with multiple slave devices (such as sensors, EEPROMs, or other microcontrollers) using only two lines:

* **SDA (Serial Data Line):** Carries the data exchanged between devices.
* **SCL (Serial Clock Line):** Synchronizes the data transfer.

Each I2C device has a **unique 7-bit or 10-bit address**.

---

## Project Purpose

The primary purpose of this project is to provide a straightforward method to:

* **Scan the I2C bus** connected to an STM32 microcontroller.
* **Identify all active I2C slave devices** by detecting their unique addresses.
* **Aid in debugging and setting up** new I2C peripherals in your embedded projects.

---

## Features

While specific features depend on the implementation details within the code, a typical I2C scanner for STM32 microcontrollers would offer:

* **Full Address Scan:** Iterates through all possible 7-bit I2C addresses (from `0x00` to `0x7F`).
* **Device Detection:** Checks for an Acknowledge (ACK) signal from a device at each probed address, indicating its presence.
* **Compatibility:** Designed for STM32 microcontrollers, likely leveraging the **STM32Cube HAL (Hardware Abstraction Layer)** or **LL (Low-Layer)** libraries for I2C communication.

---

## Project Structure

The repository contains standard **STM32CubeIDE project files**, suggesting it can be easily imported and compiled within that environment:

* `Core/`: Contains core microcontroller startup code and potentially application-specific code.
* `Drivers/`: Includes STM32 HAL/LL drivers for various peripherals, including I2C.
* `.ioc` file (e.g., `I2C_Scanner.ioc`): This is an STM32CubeMX project file, used to configure the microcontroller's peripherals and generate initialization code.

---

## How to Use

To use this I2C scanner:

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/noMoreCode4U/i2cScanner.git](https://github.com/noMoreCode4U/i2cScanner.git)
    ```
2.  **Open with STM32CubeIDE:** Import the project into STM32CubeIDE.
3.  **Configure (if necessary):** Use the `.ioc` file to review and adjust I2C peripheral settings (e.g., I2C bus pins, clock speeds) according to your specific STM32 board and hardware setup.
4.  **Compile and Flash:** Build the project and flash it onto your STM32 development board.
5.  **Monitor Output:** Connect a serial terminal to your STM32 board's UART (if the scanner outputs results via serial) to see the detected I2C addresses.

---

## Contribution

Contributions to this project are welcome! Feel free to fork the repository, make improvements, and submit pull requests.

---

## License

(Please add your desired license information here, e.g., MIT, Apache 2.0, GPL, etc.)

---
**Note:** This README is a general guide. For detailed understanding and usage, refer to the source code within the repository and the STM32CubeIDE documentation.

For more information on I2C communication with STM32 microcontrollers, you can refer to:
* [Getting started with I2C - STM32 MCU Wiki](https://wiki.st.com/stm32mcu/wiki/Getting_started_with_I2C)
* [Efficient Communication in Embedded Systems: Mastering the I2C Protocol with STM32](https://medium.com/@saimanigudla7/efficient-communication-in-embedded-systems-mastering-the-i2c-protocol-with-stm32-3682c3a14c47)
