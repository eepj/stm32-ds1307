# ds1307_for_stm32_hal
An STM32 HAL library written for the DS1307 real-time clock IC.

## To test
* Minimal setup:
```
                                             _________
                       32.768 kHz XTAL1 1 --| o       |-- 8 VCC (3V3)
                       32.768 kHz XTAL2 2 --|         |-- 7 N/C
                                    N/C 3 --|         |-- 6 SCL (PB6 for STM32F030K6)
                                    GND 4 --|_________|-- 7 SDA (PB7 for STM32F030K6)
 
 ```
* In STM32CubeIDE, include [`ds1307_for_stm32_hal.h`](./ds1307_for_stm32_hal.h) and [`ds1307_for_stm32_hal.c`](./ds1307_for_stm32_hal.c).
* Complie and flash `main.c` in [./examples](./examples) to microcontroller.
* Refer to datasheets for further information.
