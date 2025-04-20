# DIY ESP32-LLCC68 Board Pinout

This document describes the pin assignments (pinout) for the `diy_esp32-llcc68` board variant.

## General Board Features

-   **Radio:** The board uses an LLCC68 radio chip.
-   **LoRa Power:** The board is configured for 1W LoRa operation, suggesting the presence of a Power Amplifier (PA) and/or an antenna switch.
-   **Display:** The board supports an **optional** OLED display. If a display is connected, the I2C pins listed below are used.

## Radio Pins (LLCC68 - SPI)

These pins are used for communication with the LLCC68 radio module via the SPI interface and for its control.

| Function         | GPIO Pin | Description                                      |
| :--------------- | :------- | :----------------------------------------------- |
| SPI Clock        | 18       | SPI Clock line                                   |
| SPI MISO         | 19       | SPI MISO (Master In Slave Out - Data from radio) |
| SPI MOSI         | 23       | SPI MOSI (Master Out Slave In - Data to radio)   |
| Chip Select (CS) | 5        | SPI Chip Select / Slave Select                   |
| Radio Reset      | 27       | Radio module reset line                          |
| Interrupt / DIO1 | 12       | Interrupt line (IRQ) or Digital I/O 1            |
| Busy Signal      | 14       | Indicates when the radio is busy                 |
| Receive Enable   | 32       | External LNA or antenna switch control (RX mode) |
| Transmit Enable  | 25       | External PA or antenna switch control (TX mode)  |

## Optional Display Pins (OLED - I2C)

If the optional OLED display is connected, these pins are used for communication via the I2C interface.

| Function       | GPIO Pin | Description                 |
| :------------- | :------- | :-------------------------- |
| I2C Data Line  | 21       | I2C Serial Data Line (SDA)  |
| I2C Clock Line | 22       | I2C Serial Clock Line (SCL) |

---

_Note: GPIO pin values refer to the numbering used by the ESP32 microcontroller. Always verify the pinout against the specific board schematic if available._
