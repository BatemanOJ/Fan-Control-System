# Fan & LCD Controller (Mbed OS)

This project demonstrates controlling a 4-bit ST7066U LCD, a PWM-controlled fan, and a rotary encoder using the Mbed OS platform.

## Requirements
- **Board:** NUCLEO-F446RE (or equivalent STM32 with Arduino header)
- **Libraries:** `mbed.h`, `TextLCD`, `LCD_ST7066U.h`
- **Software:** Mbed CLI 2 / Mbed Studio, GCC_ARM
- **Connections:**
  | Function | MCU Pin | Notes |
  |-----------|----------|-------|
  | LCD RS | PA_6 | 4-bit interface |
  | LCD E | PA_7 |  |
  | LCD D4-D7 | PB_4, PB_5, PB_3, PA_10 |  |
  | Encoder A/B | PA_1 / PA_4 | Interrupt inputs |
  | Encoder button | BUTTON1 | |
  | Fan PWM | PB_0 | PWM output |
  | Fan tachometer | PA_0 | Interrupt input |
  | LEDs | PA_15, PB_7, PC_0, LED1 | Indicators |

## Build Instructions
```bash
mbed compile -m NUCLEO_F446RE -t GCC_ARM --flash
