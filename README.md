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
Peripheral	          MCU             Pin	Description
LCD RS	              PA_6	          Register select
LCD E	                PA_7	          Enable
LCD D4	              PB_4	          Data 4
LCD D5	              PB_5	          Data 5
LCD D6	              PB_3	          Data 6
LCD D7	              PA_10	          Data 7
Encoder A	            PA_1	          Interrupt pin A
Encoder B	            PA_4	          Interrupt pin B
Encoder Push Button	  BUTTON1	        User button on board
Fan PWM	              PB_0	          PWM output to control fan speed
Fan Tachometer	      PA_0	          Tachometer input (interrupt)
Onboard LED	          LED1 (PB_?)	    Status LED
External LED D1       PC_0	          External output indicator
LED BI Red	          PA_15	          Digital output (red)
LED BI Green	        PB_7	          Digital output (green)

## Build Instructions
```bash
mbed compile -m NUCLEO_F446RE -t GCC_ARM --flash
