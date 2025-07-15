# DIY ESP32-SX1268 Board Pinout

This document describes the pin assignments (pinout) for the `diy_esp32-sx1268` board variant.

## General Board Features

-   **Radio:** The board uses an **SX1268** radio chip.
-   **Display:** The board has an integrated display that communicates via the **I2C** interface.
-   **GPS:** A GPS module is connected to the board via the **UART** interface.
-   **Other Peripherals:** The board is equipped with a user button and a pin for battery voltage monitoring.
-   **Connectivity:** The software configuration indicates active support for **Bluetooth Classic**.

---

## Radio Pins (SX1268 - SPI & Control)

These pins are used for communication with the SX1268 radio module and for its control.

| Function               | GPIO Pin | Description                                          |
| :--------------------- | :------- | :--------------------------------------------------- |
| SPI Clock (SCLK)       | 18       | SPI Clock line                                       |
| SPI MISO               | 19       | SPI MISO (Master In Slave Out - Data from radio)     |
| SPI MOSI               | 23       | SPI MOSI (Master Out Slave In - Data to radio)       |
| Chip Select (CS)       | 5        | SPI Chip Select / Slave Select                       |
| Radio Reset            | 27       | Radio module reset line                              |
| Interrupt / DIO1       | 12       | Interrupt line (IRQ) or Digital I/O 1                |
| Busy Signal            | 14       | Indicates when the radio is busy                     |
| Receive Enable (RXEN)  | 32       | Controls an external LNA or antenna switch (RX mode) |
| Transmit Enable (TXEN) | 25       | Controls an external PA or antenna switch (TX mode)  |

---

## Display Pins (OLED - I2C)

These pins are used for communication with the OLED display via the I2C interface.

| Function             | GPIO Pin | Description                |
| :------------------- | :------- | :------------------------- |
| I2C Data Line (SDA)  | 21       | I2C Serial Data Line       |
| I2C Clock Line (SCL) | 22       | I2C Serial Clock Line      |
| Display Reset        | -1       | Reset pin is not connected |

---

## GPS Pins (UART)

These pins are used for communication with the GPS module via the UART serial interface.

| Function  | GPIO Pin | Description                                  |
| :-------- | :------- | :------------------------------------------- |
| GPS TX    | 16       | GPS Transmit line (connects to ESP32 RX pin) |
| GPS RX    | 17       | GPS Receive line (connects to ESP32 TX pin)  |
| Baud Rate | 9600 bps | Communication speed with the module          |

---

## Other Pins

| Function        | GPIO Pin | Description                                   |
| :-------------- | :------- | :-------------------------------------------- |
| Button          | 15       | Input pin for a user button                   |
| Battery Voltage | 35       | Input pin (ADC) for measuring battery voltage |

---

_Note: GPIO pin values refer to the numbering used by the ESP32 microcontroller. Always verify the pinout against the specific board schematic if available._
