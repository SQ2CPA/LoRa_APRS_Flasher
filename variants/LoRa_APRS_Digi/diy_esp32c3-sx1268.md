# DIY ESP32-C3-SX1268 Board Pinout

This document describes the pin assignments (pinout) for the `diy_esp32c3-sx1268` board variant, which is based on the ESP32-C3 microcontroller.

## General Board Features

-   **Radio:** The board uses an SX1268 radio chip.
-   **LoRa Power:** The board is configured for 1W LoRa operation, utilizing external PA/LNA control pins.

## Radio Pins (SX1268 - SPI & Control)

These pins connect the ESP32-C3 to the SX1268 radio module for SPI communication and control.

| Function         | GPIO Pin | Description                                      |
| :--------------- | :------- | :----------------------------------------------- |
| SPI Clock        | 8        | SPI Clock line                                   |
| SPI MISO         | 9        | SPI MISO (Master In Slave Out - Data from radio) |
| SPI MOSI         | 10       | SPI MOSI (Master Out Slave In - Data to radio)   |
| Chip Select (CS) | 5        | SPI Chip Select / Slave Select                   |
| Radio Reset      | 4        | Radio module reset line                          |
| Interrupt / DIO1 | 2        | Interrupt line (IRQ) or Digital I/O 1            |
| Busy Signal      | 3        | Indicates when the radio is busy                 |
| Receive Enable   | 6        | External LNA or antenna switch control (RX mode) |
| Transmit Enable  | 7        | External PA or antenna switch control (TX mode)  |

---

_Note: GPIO pin values refer to the numbering used by the ESP32-C3 microcontroller. Always verify the pinout against the specific board schematic if available._
