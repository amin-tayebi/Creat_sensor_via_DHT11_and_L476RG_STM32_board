# DHT11_sensor_data_to_L476RG_STM32_board
Transmitting Temperature and Humidity DHT11_sensor to L476RG_STM32 board
-------------------------------------------------
Note:
I wrote the codes in main.c of the project while its also possible to create a header libarary (DHT11.h) and a C library (DHT11.c) and write the fuctions on them. Then call it in the main.c.
Note:
Its possible to use DHT22 also here just you need to see the usermanual of DHT22 and compare the delay (microseconds) between the two and change that in the source code.
Note:
Its possible to use this code  in other STM32 boards. just you need to enable the TIM (timer) in the scheme of the board and then modify it corresponding to TIMER number (TIMx) every where in the code it has been used (e.g. if you enabeled TIM2 or TIM3).
-------------------------------------------------
The TIMER TIM2 with following parameters enabled:
Trigger source = ITR0
prescaler =80-1"

In the Board scheme for the signal transmission of DHT11:
PIN PA10 set to "GPIOoutput" (PIN name = A PIN number = 10)
