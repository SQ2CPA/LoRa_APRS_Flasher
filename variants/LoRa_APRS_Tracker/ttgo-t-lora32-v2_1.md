# TTGO T-LoRa32 V2.1 Board Pinout

This document describes the pin assignments (pinout) for the `ttgo-t-lora32-v2_1` board variant.

## General Board Features

-   **GPS:** A GPS module is connected to the board via the **UART** interface.
-   **Other Peripherals:** The board is equipped with a user button and a pin for battery voltage monitoring.

---

## GPS Pins (UART)

These pins are used for the UART GPS module. **Note:** GPIO 34 on the ESP32 is an input-only pin.

| Function           | GPIO Pin | Description                                  |
| :----------------- | :------- | :------------------------------------------- |
| GPS RX <- ESP32 TX | 12       | GPS Receive line (`BOARD_GPS_RX`)            |
| GPS TX -> ESP32 RX | 34       | GPS Transmit line (`BOARD_GPS_TX`)           |
| Baud Rate          | 9600 bps | Communication speed with the module          |

---

## Other Pins

| Function        | GPIO Pin | Description                                          |
| :-------------- | :------- | :--------------------------------------------------- |
| Button          | 15       | Input pin for a user button (`BOARD_BUTTON_PIN`)     |
| Battery Voltage | 35       | Input pin (ADC) for measuring battery voltage (`BOARD_BATTERY_PIN`) |

---

_Note: GPIO pin values refer to the numbering used by the ESP32 microcontroller. Always verify the pinout against the specific board schematic if available._
