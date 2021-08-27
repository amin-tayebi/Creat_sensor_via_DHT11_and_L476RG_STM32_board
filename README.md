# DHT11_sensor_data_to_L476RG_STM32_board
Transmitting Temperature and Humidity DHT11_sensor to L476RG_STM32 board
-------------------------------------------------
Note:
I wrote the codes in main.c of the project while its also possible to create a header libarary (DHT11.h) and a C library (DHT11.c) and write the fuctions on them. Ten call it in the main.c
The TIMER TIM2 with following parameters enabled:
Trigger source = ITR0
prescaler =80-1"

In the Board scheme for the signal transmission of DHT11:
PIN PA10 set to "GPIOoutput" (PIN name = A PIN number = 10)
