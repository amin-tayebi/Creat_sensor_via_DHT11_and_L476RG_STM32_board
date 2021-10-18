# DHT11_sensor_data_to_L476RG_STM32_board
<b>🔥 GOAL of the workshop</b>

Transmitting Temperature and Humidity of DHT11_sensor via L476RG_STM32 board to output (In a Terminal application)

<b>Video of deploying scenario</b>

https://drive.google.com/drive/folders/193a0y-XQt243AbnOHGVEFdcdlx3MfqSE?usp=sharing

<b>📚 Description</b>

- Based on the usermanual of DHT11 a library wrote to implement 4 steps mentioned in the usermanual to be able to read DHT11 sensor data (Temperature and Humidity) and interact with DHT11 to read it's data. 

- Pull-up and pull-down procedures for the MCU pin(MCU I/O or GPIO in/out) implemented and set them to high or low based on the DHT11 usermanual

- We Studied how define timer and related interrupt parameters. Then a timer defined to generate interrupt and delay in the board to be able to interact with DHT11 sensor and read its data 

- We wrote the codes in main.c of the project while its also possible to create a header libarary (DHT11.h) and a C library (DHT11.c) and write the fuctions on them and locate these files on the Src Folder (where other header libraries exist). Then call x.h file in the main.c (e.g. Include DHT11.h).

- Its possible to use DHT22 also here just you need to see the usermanual of DHT22 and compare the delay (microseconds) between the two and change that in the source code.

- Its possible to use this code in other STM32 boards. Just you need to enable one of the timers in the scheme configuration page (of the board) and set its parameters based on the video, then it needs to be same as every where in the code it has been used (e.g. if you enabeled timer3 (TIM3) then in compare to this maic.c file every where it shold be TIM3).

- All of the timers are equal we need to activate and set configuration just on one of them (makes no different TIM2 TM3 or....).

- We didn't put other codes (main.h or stm32l4xx_hal.h and other...) as they are remained unchanged.

Here the TIMER TIM2 with following parameters enabled:

Trigger source = ITR0

prescaler = 80-1

In the Board scheme for the signal transmission of DHT11:
PIN PA10 set to "GPIOoutput" (PIN name = A PIN number = 10)

<b>👉 Hardware equipment</b>

- DHT11_sensor

- L476RG_STM32 board

- Related USB cable (connect board to the PC)

- 3*Jumper wires

<b>👉 Software equipment</b>

- Cube-IDE software

- Cutecome terminal application (or any terminal application)

<b>👋 Additional resources</b>

Links for downloading STM-cube-IDE:

https://www.st.com/en/development-tools/stm32cubeide.html

L476RG_STM32_BOARD documentation and user manual:

https://www.st.com/resource/en/user_manual/um1724-stm32-nucleo64-boards-mb1136-stmicroelectronics.pdf

L476RG_STM32_BOARD pins out:

https://os.mbed.com/platforms/ST-Nucleo-L476RG/

DHT11 usermanual:

https://www.mouser.com/datasheet/2/758/DHT11-Technical-Data-Sheet-Translated-Version-1143054.pdf
