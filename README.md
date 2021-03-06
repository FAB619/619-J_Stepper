<div align="center"><h1 style="font-family: courier;" align="center">619-J_Stepper</h1></div>
<div align="center"><img src="image/closed loop.26.jpg" width="70%"></div>
<div align="center"><b>An open source closed loop stepper driver.</b></div>

# 619-J_Stepper
**619-J_Stepper** is an open source micro-controller board used to drive a stepper motor in closed loop mode. The board is generally used on 3D printer steppers or CNC steppers to prevent losing steps. The project is inspired by [**Tropical labs: Mechaduino board**](https://tropical-labs.com/mechaduino/).

Here the **features** of the **619-J_Stepper**:

* **STM32F103C8T6 ARM 32-bit Cortex™-M3** is the CPU of the board. Higher frequency, higher speed and cost-effictive.  

* **Magnetic encoder to Allegro's A1333LLETR-T** Contactless 0° to 360° angle sensor IC ,12bit

* **USB programming** and **serial communication** (serial version)

* High speed printing without losing steps.

* Ported the compilation platform from arduino to PlatformIO —— Convenient for STM32 MCU compilation

* This project support build and upload by platformio, you can use Atom or Code editor (need install platformio) build it or upload firmware.

* Cosed loop motor feedback.

Here are the schematic and the board:

<div align="center"><img src="image/sch.JPG" width="100%"></div>


<div align="center"><img src="image/brd.JPG" width="100%"></div>

<div align="center"><img src="image/3d.JPG" width="100%"></div>



<iframe src="https://myhub.autodesk360.com/ue2824bfc/shares/public/SH919a0QTf3c32634dcfc82b0b883f1f9a82?mode=embed" width="640" height="480" allowfullscreen="true" webkitallowfullscreen="true" mozallowfullscreen="true"  frameborder="0"></iframe>

# Manufacturing

After finishing the Routing and verify the pcb. We made the board at **[JLC PCB](https://jlcpcb.com/)**  and we chose also the PCB Assembly service which was very good.

<div align="center"><img src="image/placev2.gif" width="100%"></div>


Here is the **[BOM needed](https://github.com/FAB619/619-J_Stepper/blob/main/files/BOM_final.xlsx)** for jlcpcb assembly service:

<div align="center"><img src="image/bom gif.gif" width="100%"></div>


# Downloads

* [619-J_Stepper schematics](https://github.com/FAB619/619-J_Stepper/tree/main/files/Kicad%20Files)

* [619-J_Stepper board](https://github.com/FAB619/619-J_Stepper/tree/main/files/Kicad%20Files)

* [619-J_Stepper Step](https://github.com/FAB619/619-J_Stepper/blob/main/files/Stepper%20Servo.step)

* [619-J_Stepper BOM](https://github.com/FAB619/619-J_Stepper/blob/main/files/BOM_final.xlsx)

* [619-J_Stepper Position file](https://github.com/FAB619/619-J_Stepper/blob/main/files/Stepper%20Servo-all-pos.csv)

* [619-J_Stepper Gerber](https://github.com/FAB619/619-J_Stepper/tree/main/files/Manufacturing)

# Getting started

To program the board, It is necessary to use an **ST-link v2** Programmer (or a **J-Tag**) using also [ST-link Utility](https://www.st.com/en/development-tools/stsw-link004.html). You can find the **Bin File** we will use to flash the stm32 at this [link](https://github.com/FAB619/619-J_Stepper/tree/main/Bin%20File).

If you don't have an St-link you can use any stm32 board as a programmer as shown in this [link](https://geekilyinteresting.wordpress.com/2014/05/04/using-your-stm32f4-discovery-board-as-a-programmer-and-debugger/)

## Wiring

Use an ST-link to connect to **619-J_Stepper**  

<div align="center"><img src="image/stlink.jpg" width="100%"></div>

<div align="center"><img src="image/swd.png" width="100%"></div>

<div align="center"><img src="image/swd1.jpeg" width="100%"></div>

## Connect PC upload firmware
Need to connect STlink's SWDIO,SWCLK,RESET,GND to 619-J_Stepper motherboard's SWDIO,SWCLK,RESET,GND.

If you are using Slink for the first time, you may need to install the driver,Upload firmware by slink.

<div align="center"><img src="image/peri.PNG" width="100%"></div>

<div align="center"><img src="image/1.PNG" width="100%"></div>

<div align="center"><img src="image/2.PNG" width="100%"></div>

Connect to your board, you will notice that the sftware recognize your board and shows the memory of the MCU, and the St-link will blink in two diffrent colors.

<div align="center"><img src="image/3'.PNG" width="100%"></div>

 Now you can porceed with loading the **Bin File**

<div align="center"><img src="image/3.PNG" width="100%"></div>

Upload to your board.

<div align="center"><img src="image/4.PNG" width="100%"></div>

<div align="center"><img src="image/5.png" width="100%"></div>

**Done**, Program uploaded successfully and an LED will turn on. This means a board programed.

<div align="center"><img src="image/6.PNG" width="100%"></div>

<div align="center"><img src="image/7.jpeg" width="100%"></div>

# Video

<div align="center"><img src="image/test vid.mp4" width="100%"></div>




# License

The hardware is under the Creative Commons Attribution Share-Alike 4.0 License as much of the work is based on Mechaduino project by J. Church.

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Licence Creative Commons" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />Ce(tte) œuvre est mise à disposition selon les termes de la <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Licence Creative Commons Attribution - Pas d’Utilisation Commerciale - Partage dans les Mêmes Conditions 4.0 International</a>.

# Disclaimer

This hardware/software is provided "as is", and you use the hardware/software at your own risk. Under no circumstances shall any author be liable for direct, indirect, special, incidental, or consequential damages resulting from the use, misuse, or inability to use this hardware/software, even if the authors have been advised of the possibility of such damages.
