# DHT11_sensor_data_to_L476RG_STM32_board
<b>🔥🔥🔥 GOAL of the project:</b>

Transmitting Temperature and Humidity of DHT11_sensor via L476RG_STM32 board to output (In a Terminal application)


<b>👉 Hardware equipment:</b>

- DHT11_sensor

- L476RG_STM32 board

- Related USB cable (connect board to the PC)

- 3*Jumper wires

<b>👉 Software equipment:</b>

- Cube-IDE software

- Cutecome terminal application (or any terminal application)

<b>📚 Description:</b>

- I wrote the codes in main.c of the project while its also possible to create a header libarary (DHT11.h) and a C library (DHT11.c) and write the fuctions on them. Then call it in the main.c.

- Its possible to use DHT22 also here just you need to see the usermanual of DHT22 and compare the delay (microseconds) between the two and change that in the source code.

- Its possible to use this code  in other STM32 boards. Just you need to enable the TIM (timer) in the scheme of the board, then modify and correspond it to the TIMER number (TIMx) every where in the code it has been used (e.g. if you enabeled TIM2 or TIM3).

Here the TIMER TIM2 with following parameters enabled:

Trigger source = ITR0

prescaler =80-1"

In the Board scheme for the signal transmission of DHT11:
PIN PA10 set to "GPIOoutput" (PIN name = A PIN number = 10)

<b>Related video:</b>

https://drive.google.com/drive/folders/193a0y-XQt243AbnOHGVEFdcdlx3MfqSE?usp=sharing


<b>👋 Additional resources</b>

Links for downloading STM-cube-IDE:

https://www.st.com/en/development-tools/stm32cubeide.html

L476RG_STM32_BOARD documentation and user manual:

https://www.st.com/resource/en/user_manual/um1724-stm32-nucleo64-boards-mb1136-stmicroelectronics.pdf

L476RG_STM32_BOARD pins out:

https://os.mbed.com/platforms/ST-Nucleo-L476RG/

DHT11 usermanual:

https://www.mouser.com/datasheet/2/758/DHT11-Technical-Data-Sheet-Translated-Version-1143054.pdf
