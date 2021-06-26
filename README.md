# DS1307_for_STM32_HAL
An STM32 HAL library for the DS1307 real-time clock IC.

## To test
* Minimal setup:
```
                                             _________
                       32.768 kHz XTAL1 1 --| o       |-- 8 VDD
                       32.768 kHz XTAL2 2 --|         |-- 7 N/C
                                    N/C 3 --|         |-- 6 SCL1
                                    GND 4 --|_________|-- 5 SDA1
 
 ```
* In STM32CubeIDE, include [`ds1307_for_stm32_hal.h`](./ds1307_for_stm32_hal.h) and [`ds1307_for_stm32_hal.c`](./ds1307_for_stm32_hal.c).
* Complie and flash [`main.c`](./examples/main.c) in [`./examples`](./examples) to microcontroller.
* Read the results from a UART monitor.
* Refer to [datasheets](https://www.maximintegrated.com/en/products/analog/real-time-clocks/DS1307.html) for further information.

## Note
* Avoid writing to registers 00h to 10h as those are reserved for this library.

## Known issues
* Day of week fails to update at mindnight on March 1, 2020. This does not appear to recur in any other leap year.
