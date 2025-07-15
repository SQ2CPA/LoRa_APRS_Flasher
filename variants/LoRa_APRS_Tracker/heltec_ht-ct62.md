# Heltec HT-CT62 Board Pinout

This document describes the pin assignments (pinout) for the `heltec_ht-ct62` board variant.

## General Board Features

-   **Radio:** The board uses an **SX1262** radio chip.
-   **Display:** The board has an integrated **OLED display** that communicates via the **I2C** interface.
-   **GPS:** A GPS module is connected to the board via the **UART** interface.
-   **Other Peripherals:** The board includes a pin for battery voltage monitoring.

---

## Radio Pins (SX1262 - SPI & Control)

These pins are used for communication with the SX1262 radio module.

| Function         | GPIO Pin | Description                                      |
| :--------------- | :------- | :----------------------------------------------- |
| SPI Clock (SCLK) | 10       | SPI Clock line                                   |
| SPI MISO         | 6        | SPI MISO (Master In Slave Out - Data from radio) |
| SPI MOSI         | 7        | SPI MOSI (Master Out Slave In - Data to radio)   |
| Chip Select (CS) | 8        | SPI Chip Select / Slave Select                   |
| Radio Reset      | 5        | Radio module reset line                          |
| Interrupt / DIO1 | 3        | Interrupt line (IRQ) or Digital I/O 1            |
| Busy Signal      | 4        | Indicates when the radio is busy                 |

---

## Display Pins (OLED - I2C)

These pins are used for the I2C OLED display.

| Function        | GPIO Pin | Description                |
| :-------------- | :------- | :------------------------- |
| I2C Data (SDA)  | 18       | I2C Serial Data Line       |
| I2C Clock (SCL) | 19       | I2C Serial Clock Line      |
| Display Reset   | -1       | Reset pin is not connected |

---

## GPS Pins (UART)

These pins are used for the UART GPS module.

| Function           | GPIO Pin | Description                                  |
| :----------------- | :------- | :------------------------------------------- |
| GPS TX -> ESP32 RX | 1        | GPS Transmit line (connects to ESP32 RX pin) |
| GPS RX <- ESP32 TX | 0        | GPS Receive line (connects to ESP32 TX pin)  |
| Baud Rate          | 9600 bps | Communication speed with the module          |

---

## Other Pins

| Function        | GPIO Pin | Description                                   |
| :-------------- | :------- | :-------------------------------------------- |
| Battery Voltage | 2        | Input pin (ADC) for measuring battery voltage |

---

_Note: GPIO pin values refer to the numbering used by the ESP32 microcontroller. Always verify the pinout against the specific board schematic if available._
