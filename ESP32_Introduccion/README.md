# Para programar con micropython
## Instalar el firmware
1. Lo primero que hay que hacer al momento de querer trabajar con un ESP32 es buscar y descargar un firmware que establezca la forma en la cual manejaremos nuestro microcontrolador, para este caso, buscamos un firmware con el cual podamos programar en micropython. Podemos simplemente descargar el primer resultado que de confianza y que cumpla con nuestros requisitos, por ejemplo: [Firmware de micropython](https://github.com/russhughes/st7789s3_mpy)
2. Una vez obtenido un firmware, necesitamos una herramienta que nos ayude a cargar dicho firmware en nuestro ESP32, para ello, utilizaremos la [herramienta oficial de Espressif](https://www.espressif.com/en/support/download/other-tools?keys=), seleccionaremos el modelo de nuestro ESP32, la opcion "Flash Download Tools" y finalmente haremos clic en "Download Selected".
![Screenshot de la pagina Espressif](https://github.com/OscSerrano/Invernada_Robotica/blob/main/ESP32_Introduccion/Imagenes/ESP32T1.png)
3. Ejecutamos nuestra herramienta, que nos pedira el modelo de nuestra ESP32, el modo en que queremos utilizarlo y el protocolo de ocmunicacion a utilizar para comunicarse con el controlador. Una vez ingresados esos 3 datos, ahora nos aparecera una tabla en la que el primer elemento pondremos el firmware que descargamos, a su derecha la direccion de memoria que ocupara, es decir 0, colocaremos una palomita en el recuadro de la izquierda, seleccionaremos el puerto al que esta conectado el ESP32, aumentaremos los baudios a 921600 y, ahora en la placa fisica, tendremos que presionar el boton de boot, sin soltarlo presionar el boton de reset, soltamos reset y, todavia sin soltar boot, hacemos clic en el boton de "Start" en la herramineta para empezar a flashear el firmware, una vez iniciado el proceso, podemos soltar el boton de boot y esperar a que termine de flashear.
![Screenshot de la herramienta Espressif](https://github.com/OscSerrano/Invernada_Robotica/blob/main/ESP32_Introduccion/Imagenes/ESP32T2.png)
## Instalar un IDE de micropython
La opcion mas recomendable para programar con micropython y ESP32 es utilizar [Thonny IDE.](https://thonny.org)

Esto porque una vez instalado, todo lo que hay que hacer es seleccionar el interprete correcto, que en nuestro caso es ESP32, y luego seleccionar el puerto al que esta conectado nuestro controlador.
![Screenshot de la herramienta Espressif](https://github.com/OscSerrano/Invernada_Robotica/blob/main/ESP32_Introduccion/Imagenes/ESP32T3.png)


# IDEs para programar en C/C++
## PlatformIO IDE
### Descripcion
Entorno de desarrollo profesional para Embebidos, IoT, Arduino, CMSIS, ESP-IDF, FreeRTOS, libOpenCM3, mbed OS, Pulp OS, SPL, STM32Cube, Zephyr RTOS, ARM, AVR, Espressif (ESP8266/ESP32), FPGA, MCS-51 ( 8051), MSP430, Nórdico (nRF51/nRF52), PIC32, RISC-V, STMicroelectronics (STM8/STM32), Teensy
### Requerimientos
+ [Python](https://www.python.org/downloads/)
+ [Visual Studio Code](https://code.visualstudio.com/download)
+ [Instalar la extension "PlatformIO" en VS Code](https://marketplace.visualstudio.com/items?itemName=platformio.platformio-ide)
### Primeros pasos
1. Despues de instalar la extension PlatformIO y tras reiniciar o recargar Visual Studio Code, nos aparecera un nuevo simbolo en la barra de la izquierda (el logo de PlatformIO), al presionarlo aparecera un nuevo menu, dle cual debemos seleccionar la pestaña llamada "platforms".
![Screenshot menu de PlatformIO](https://github.com/OscSerrano/Invernada_Robotica/blob/main/ESP32_Introduccion/Imagenes/ESP32P1.png)
2. En la nueva pagina que se salio debemos seleccionar la pestaña "Embedded", buscar la opcion que diga "Espressif 32" y hacer clic sobre esa opcion para ver los diferentes modelos de ESP32 disponibles.
![Screenshot menu de PlatformIO](https://github.com/OscSerrano/Invernada_Robotica/blob/main/ESP32_Introduccion/Imagenes/ESP32P2.png)
3. En esta parte saldran todas las versiones de ESP32 para las que PlatformIO tiene soporte, por ello, debemos buscar nuestro modelo de ESP32 y una vez que lo encontremos debemos hacer clic en el boton Install para instalar el manejador de nuestro controlador.
![Screenshot menu de PlatformIO](https://github.com/OscSerrano/Invernada_Robotica/blob/main/ESP32_Introduccion/Imagenes/ESP32P3.png)
4. Con esto, finalmente hemos completado la instalacion de PlatformIO IDE y estamos listo para empezar nuestros proyectos con nuestro EP32. Para ello, debemos ir a la pestaña "Home" y elegir entre hacer un nuevo proyecto o cargar uno ya hecho.
![Screenshot menu de PlatformIO](https://github.com/OscSerrano/Invernada_Robotica/blob/main/ESP32_Introduccion/Imagenes/ESP32P4.png)





