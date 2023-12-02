# IDE de Arduino
## Descripcion
El entorno de desarrollo integrado (IDE) de Arduino es una aplicación multiplataforma (para Windows, macOS, Linux ) que está escrita en el lenguaje de programación Java. Se utiliza para escribir y cargar programas (de C y C++) en placas compatibles con Arduino, pero también, con la ayuda de núcleos de terceros, se puede usar con placas de desarrollo de otros proveedores como ESP32.
## Instalacion
Para realizar la instalacion se debe seguir el [Tutorial para descargar e instalar Arduino IDE 2](https://docs.arduino.cc/software/ide-v2/tutorials/getting-started/ide-v2-downloading-and-installing)
## Primeros pasos
Despues de descargar e instalar correctamente el entorno de desarrollo de Arduino, debemos abrir el IDE de Arduino y conectar la tablilla a la computadora. Tras lo cual debemos asegurarnos de hacer los siguientes 2 pasos para poder utilizar nuestro Arduino.
1. Lo primero que debemos hacer es seleccionar el modelo de Arduino que estamos utilizando.
![Screenshot seleccionando la placa de desarrollo Arduino](https://github.com/OscSerrano/Invernada_Robotica/blob/main/Arduino_Basico/Imagenes/ArduinoB1.png)
2. Finalmente tenemos que seleccionar el puerto al cual fue asignado nuestro Arduino tras haberlo conectado a la computadora.
![Screenshot seleccionando el puerto donde esta el Arduino](https://github.com/OscSerrano/Invernada_Robotica/blob/main/Arduino_Basico/Imagenes/ArduinoB2.png)
3. Una vez que el mensaje de abajo a la derecha nos dice que el Arduino se ha conectado correctamente, entonces podemos empezar a programar nuestra tablilla. Al tener el programa escrito, podemos utilizar el primer boton de arriba a la izquierda para compilar y verificar errores con el programa. Despues debemos usar el boton a su derecha para cargar el programa en el Arduino
![Screenshot mostrando btones y mensajes relacionados al texto](https://github.com/OscSerrano/Invernada_Robotica/blob/main/Arduino_Basico/Imagenes/ArduinoB3.png)

# Manual de primeras practicas 
## Practica 1: Lectura digital
### Materiales
+ 1 Arduino
+ 1 Breadboard
+ 1 Boton
+ 1 Resistencia de 10k ohms
### Circuito
![Esquematico de la practica 1](https://github.com/OscSerrano/Invernada_Robotica/blob/main/Arduino_Basico/Imagenes/CircuitoB1.png)
### Codigo
![Codigo de la practica 1](https://github.com/OscSerrano/Invernada_Robotica/blob/main/Arduino_Basico/Imagenes/CodigoB1.png)
### Practicas relacionadas
+ Cambiar INPUT a INPUT_PULLUP
+ Contador de pulsasiones por minuto
+ Crear un flip flop

## Practica 2: Lectura analogica
### Materiales
+ 1 Arduino
+ 1 Breadboard
+ 1 Potenciometro de 10k ohms
### Circuito
![Esquematico de la practica 2](https://github.com/OscSerrano/Invernada_Robotica/blob/main/Arduino_Basico/Imagenes/CircuitoB2.png)
### Codigo
![Codigo de la practica 2](https://github.com/OscSerrano/Invernada_Robotica/blob/main/Arduino_Basico/Imagenes/CodigoB2.png)
### Practicas relacionadas
+ Obtener la lectura de voltaje del potenciometro
+ Emular la entrada de un sensor en el monitor serial

## Practica 3: Salida digital (LED parpadeante)
### Materiales
+ 1 Arduino
+ 1 Breadboard
+ 1 Foco LED
+ 1 Resistencia de 220 ohms
### Circuito
![Esquematico de la practica 3](https://github.com/OscSerrano/Invernada_Robotica/blob/main/Arduino_Basico/Imagenes/CircuitoB3.png)
### Codigo
![Codigo de la practica 3](https://github.com/OscSerrano/Invernada_Robotica/blob/main/Arduino_Basico/Imagenes/CodigoB3.png)
### Practicas relacionadas
+ Controlar el parpadeo con la entrada digital
+ Controlar el parpadeo con la entrada analogica
+ Hacer que el parpadeo sea codigo morse (o alguna otra secuencia con más leds)

## Practica 4: Salida analogica (LED desvaneciente)
### Materiales
+ 1 Arduino
+ 1 Breadboard
+ 1 Foco LED
+ 1 Resistencia de 220 ohms
### Circuito
![Esquematico de la practica 4](https://github.com/OscSerrano/Invernada_Robotica/blob/main/Arduino_Basico/Imagenes/CircuitoB4.png)
### Codigo
![Codigo de la practica 4](https://github.com/OscSerrano/Invernada_Robotica/blob/main/Arduino_Basico/Imagenes/CodigoB4.png)
### Practicas relacionadas
+ Controlar el brillo del led con la entrada analogica
+ Crear una secuencia de leds desvanecientes
+ Crear luces navideñas con varias secuencias guardadas

## Practicas adicionales de desafio
+ Crear un contador binario
+ Crear un semaforo
+ Crear un juego de memoria estilo Simon


