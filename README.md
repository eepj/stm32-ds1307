# ds1307_for_stm32_hal
A DS1307 real-time clock library written with STM32 HAL.

# To test
Minimal setup:
```
                                             _________
                       32.768 kHz XTAL1 1 --| o       |-- 8 VCC (3V3)
                       32.768 kHz XTAL2 2 --|         |-- 7 N/C
                                    N/C 3 --|         |-- 6 SCL (PB6 for STM32F030K6)
                                    GND 4 --|_________|-- 7 SDA (PB7 for STM32F030K6)
 
 ```
* Complie and download example.
* Refer to datasheets for further information.
