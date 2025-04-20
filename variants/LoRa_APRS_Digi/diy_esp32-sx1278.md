# DIY ESP32-SX1278 Board Pinout

This document describes the pin assignments (pinout) for the `diy_esp32-sx1278` board variant.

## General Board Features

-   **Radio:** The board uses an SX1278 radio chip.
-   **Display:** The board supports an **optional** OLED display. If a display is connected, the I2C pins listed below are used.
-   **Internal LED:** An **optional** onboard LED is connected to GPIO 2.

## Radio Pins (SX1278 - SPI & Control)

These pins are used for communication with the SX1278 radio module via the SPI interface and for its control.

| Function          | GPIO Pin | Description                                      |
| :---------------- | :------- | :----------------------------------------------- |
| SPI Clock (SCK)   | 5        | SPI Clock line                                   |
| SPI MISO          | 19       | SPI MISO (Master In Slave Out - Data from radio) |
| SPI MOSI          | 27       | SPI MOSI (Master Out Slave In - Data to radio)   |
| Chip Select (CS)  | 18       | SPI Chip Select / Slave Select                   |
| Radio Reset (RST) | 14       | Radio module reset line                          |
| Interrupt / DIO0  | 26       | Radio Interrupt line (IRQ - typically DIO0)      |

## Optional Display Pins (OLED - I2C)

If the optional OLED display is connected, these pins are used for communication via the I2C interface.

| Function       | GPIO Pin | Description                 |
| :------------- | :------- | :-------------------------- |
| I2C Data Line  | 21       | I2C Serial Data Line (SDA)  |
| I2C Clock Line | 22       | I2C Serial Clock Line (SCL) |

---

_Note: GPIO pin values refer to the numbering used by the ESP32 microcontroller. Always verify the pinout against the specific board schematic if available._
