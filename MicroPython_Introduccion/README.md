# Programacion en micropython
## Librerias / Modulos
### import machine
Esta libreria contiene funciones que permiten acceder y controlar el hardware y el sistema de nuestro controlador. 

Dentro de este modulo podemos encontrar las siguientes clases o submodulos y sus metodos mas relevantes:
+ machine.Pin -> Permite controlar las salidas y entradas de proposito general.
  + `machine.Pin(**id, mode, pull, value, drive, alt**)` -> Sirve para definir un pin de nuestra placa y poder utilizarlo despues.
  + `Pin.init(**mode, pull, value, drive, alt**)` -> Sirve para reconfigurar un pin.
    + **mode** -> Puede ser Pin.IN, Pin.OUT, Pin.ANALOG
    + **pull** -> Puede ser None, Pin.PULL_UP o Pin.PULL_DOWN.
    + **value** -> Inicializa la salida en 0 o 1.
    + **drive** -> Sirve para definir la cantidad de corriente del pin, puede ser Pin.DRIVE_0, Pin.DRIVE_1 o Pin.DRIVE_2.
  + `Pin.on()` y `Pin.high()` -> Hace que la salida del pin sea 1.
  + `Pin.off()` y `Pin.low()` -> Hace que la salida del pin sea 0.
  + `Pin.irq(**handler, trigger, priority, wake, hard**)` -> Configura una interrupcion.
    + **handler** -> Es la funcion que se va a llamar cuando se dispare la interrupcion.
    + **trigger** -> Define el evento que provoca la interrupcion. Puede ser Pin.IRQ_FALLING, Pin.IRQ_RISING, Pin.IRQ_LOW_LEVEL y/o Pin.IRQ_HIGH_LEVEL.
    + **priority** -> Numero que define la prioridad de la interrupcion, aquella con más prioridad no puede ser interrumpida por una de menor prioridad.

+ machine.ADC -> Permite leer entradas analogicas convirtiendolas en digitales.
  + `machine.ADC(**id, sample_ns, atten**)` -> Sirve para utilizar un pin (id) de nuestra placa en modo de entrada analogica.
  + `ADC.init(**sample_ns, atten**)` -> Sirve para reconfigurar un adc.
    + **id** -> Es el machine.Pin que queremos utilizar.
    + **sample_ns** -> Es el tiempo de muestreo en nanosegundos.
    + **atten** -> Especifica la atenuacion del input, que puede ser ADC.ATTN_0DB, ADC.ATTN_2_5DB, ADC.ATTN_6DB o ADC.ATTN_11DB.
  + `ADC.read()`, `ADC.read_u16()` y `ADC.read_uv()` -> Sirven para leer los voltios y microvoltios respectivamente de una señal analogica.
   
+ machine.PWM -> Permite usar salidas analogicas.
  + `machine.PWM(**dest, freq, duty_u16, duty_ns, invert**)` -> Asigna salida analogica en un pin.
  + `PWM.init(freq, duty_u16, duty_ns)` -> Sirve para reconfigurar el PWM.
    + **dest** -> Es el machine.Pin que queremos utilizar.
    + **freq** -> Establece la frecuencia del pulso pwm en Hz.
    + **duty, duty_u16 o duty_ns** -> Controla la proporción de tiempo que el pulso está en estado alto.
  + `PWM.deinit()` -> Sirve para deshabilitar el PWM de un pin.

### import time
Esta libreria contiene funciones que permiten obtener la fecha y hora actual, para medir intervalos de tiempo, asi como para hacer delays.

Dentro de este modulo podemos encontrar las siguientes clases o submodulos y sus metodos mas relevantes:
+ `time.sleep()`, `time.sleep_ms()` y `time.sleep_us()` -> Se usa para detener el programa por una cantidad de tiempo en segundos, milisegundos y microsegundos respectivamente.
+ `time.ticks_ms()`, `time.ticks_us()` y `time.ticks_cpu()` -> Devuelve la cantidad de milisegundos, de nanosegundos y de ciclos de reloj respectivamente, que han pasado desde el inicio de la placa.
+ `time.ticks_diff(ticks1, ticks2)` -> Devuelve la diferencia entre dos ticks, ya sea en milisegundos, nanosegundos o ciclos de reloj.
+ `time.ticks_add(ticks1, delta)` -> Devuelve la suma entre un tick y un numero que se ajusta a las unidades del tick, ya sea en milisegundos, nanosegundos o ciclos de reloj.
+ `time.time()` y `time.time_ns()` -> Devuelve la cantidad de segundos y de nanosegundos, respectivamente, desde que se encendio el controlador.

### Otras librerias que podrian ser utiles en el futuro
+ `import random`
+ `import Timer`
+ `import UART`
+ `import SPI / import SoftSPI`
+ `import I2C / import SoftI2C`
+ `import WDT (Watchdog timer)`

## Variables / Tipos de datos
En Python no es necesario declarar explicitamente el tipo de las variables a utilizar, es decir, podemos hacer `variable = 1` en lugar de `int variable = 1`, de esta manera podemos decir que Python asigna el tipo de dato automaticamente, por ello, no hace falta preocuparse por las variables básicas:
+ `str`
+ `int`
+ `float`
+ `bool`

##Colecciones / Arreglos
+ **Tuple** (Tuplas)
  +  Se declara con parentesis asi: `datos = (1, 2, "Hola", True, 3)`
  +  Acepta tipos de datos diferentes dentro de si mismo
  +  Una vez creado ya no se puede modificar de ninguna manera
  +  Se puede usar el constructor `tuple()` para crearlo
+ **List** (Listas)
  +  Se declara con corchetes asi: `datos = [1, 2, "Hola", True, 3]`
  +  Acepta tipos de datos diferentes dentro de si mismo
  +  Una vez creado, existen las funciones `append, insert, remove, pop, sort, reverse y clear` para modificar la lista por completo
  +  Se puede usar el constructor `list()` para crearlo
+  **Set** (Conjuntos)
  +  Se declara con llaves asi: `datos = {1, 2, "Hola", True, 3}`
  +  Acepta tipos de datos diferentes dentro de si mismo
  +  No acepta valores duplicados (como 1 se puede considerar True y 0 False, se debe tener cuidado)
  +  No tiene indices
  +  Se pueden hacer operaciones de conjuntos con `union, intersection y difference`
  +  Una vez creado, existen las funciones `add, remove, pop y clear` para modificarlo
  +  Se puede usar el constructor `set()` para crearlo
+ **Dictionary** (Diccionarios)
  +  Se declara con llaves asi: `datos = {"Nombre": "Oscar", "Edad": 21, 13: True}`, de forma que el primer valor es una llave (key) y el segundo es el valor asignado (value)
  +  La llave actua como el indice, es decir que, escribir `datos["Nombre"]` seria acceder al primer elemento del diccionario anterior y `datos[13]` al tercero
  +  Acepta tipos de datos diferentes dentro de si mismo
  +  Los valores se pueden modificar libremente
  +  Se usan las funciones `keys, values y items` para obtener una lista con los elementos solicitados
  +  Siempre y cuando no se repitan las llaves, el diccionario se puede expandir
  +  Se usa el prefijo `del` para borrar una llave del diccionario o `clear` para borrarlo todo
+  **Range** (Rangos)
  +  Tiene que declararse implicitamente asi: `Range(start, end, step)` donde "start" es el numero donde empieza el rango (si no lo pones, por defecto es 0), "end" es donde termina el rango (este valor si es necesario ponerlo) y "step" es la suma o resta que se debe hacer para ir de inicio a fin del rango (si no se pone, por defecto es 1).
  +  Solo acepta enteros
  +  El rango se produce una sola vez y solo si se utiliza.

## Operadores
### Operadores aritmeticos
+ Suma: `+`
+ Resta: -
+ Multiplicacion: `*`
+ Division: `/`
+ Modulo: `%`
+ Exponenciacion: `**`

### Operadores comparativos
+ Igual: `==`
+ Diferente: `!=`
+ Mayor que: `>`
+ Menor que: `<`

### Operadores binarios
+ AND: `&`
+ OR: `|`
+ NOT: `~`
+ Left Shift: `<<`
+ Right Shift: `>>`

## Estructuras de control de flujo
### Condicionales
La estructura de los if's cambia ligeramente en Python, concretamente, ya no se necesitan parentesis en la condicion, se utiliza `:` para definir el inicio del if y, finalmente, en lugar de tener que escribir `else if`, debemos escribir `elif` en su lugar.
+ `if condicion1:`
+ `elif condicion2:`
+ `else:`

### Bucles
+ `for elemento in lista:`

En Python los for's son completamente diferentes, para poder utilizarlos necesitas tener si o si una de las colecciones de Python (Lista, Tupla, Rango, Diccionario o Conjunto), de esta manera, el ciclo for recorrera la coleccion guardando el valor en la variable designada para cada iteracion del ciclo.
+ `while condicion:`

Por otra parte el ciclo while solo tiene el cambio de necesitar dos puntos en lugar de llaves para funcionar, todo lo demas es igual que en otros lenguajes, el ciclo continua repitiendose mientras la condicion se cumpla.

## Funciones
Al igual que con las variables, las funciones ni sus parametros necesitan declararse implicitamente, si no que Pytohn lo hara automaticamente. Por ello la declaracion se hace de la siguiente manera:
+ `def funcion(parametros):`

Finalmente, dependiendo de si necesitas una funcion o un metodo, puedes poner o no el comando `return`

  
