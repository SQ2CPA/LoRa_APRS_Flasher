# DIY ESP32-SX1278 Board Pinout

This document describes the pin assignments (pinout) for the `diy_esp32-sx1278` board variant.

## General Board Features

-   **Radio:** The board uses an **SX1278** radio chip.
-   **Display:** The board has an integrated **OLED display** with a dedicated reset pin, communicating via **I2C**.
-   **GPS:** A GPS module is connected to the board via the **UART** interface.
-   **Other Peripherals:** The board is equipped with a user button and a pin for battery voltage monitoring.
-   **Connectivity:** The software configuration indicates active support for **Bluetooth Classic**.

---

## Radio Pins (SX1278 - SPI & Control)

These pins are used for communication with the SX1278 radio module.

| Function          | GPIO Pin | Description                                      |
| :---------------- | :------- | :----------------------------------------------- |
| SPI Clock (SCK)   | 5        | SPI Clock line                                   |
| SPI MISO          | 19       | SPI MISO (Master In Slave Out - Data from radio) |
| SPI MOSI          | 27       | SPI MOSI (Master Out Slave In - Data to radio)   |
| Chip Select (CS)  | 18       | SPI Chip Select / Slave Select                   |
| Radio Reset (RST) | 23       | Radio module reset line                          |
| Interrupt / DIO0  | 26       | Radio Interrupt line (IRQ - typically DIO0)      |

---

## Display Pins (OLED - I2C)

These pins are used for the I2C OLED display.

| Function        | GPIO Pin | Description               |
| :-------------- | :------- | :------------------------ |
| I2C Data (SDA)  | 21       | I2C Serial Data Line      |
| I2C Clock (SCL) | 22       | I2C Serial Clock Line     |
| Display Reset   | 16       | Display module reset line |

---

## GPS Pins (UART)

These pins are used for the UART GPS module. **Note:** GPIO 34 on the ESP32 is an input-only pin.

| Function           | GPIO Pin | Description                                  |
| :----------------- | :------- | :------------------------------------------- |
| GPS TX -> ESP32 RX | 34       | GPS Transmit line (connects to ESP32 RX pin) |
| GPS RX <- ESP32 TX | 12       | GPS Receive line (connects to ESP32 TX pin)  |
| Baud Rate          | 9600 bps | Communication speed with the module          |

---

## Other Pins

| Function        | GPIO Pin | Description                                   |
| :-------------- | :------- | :-------------------------------------------- |
| Button          | 15       | Input pin for a user button                   |
| Battery Voltage | 35       | Input pin (ADC) for measuring battery voltage |

---

_Note: GPIO pin values refer to the numbering used by the ESP32 microcontroller. Always verify the pinout against the specific board schematic if available._
