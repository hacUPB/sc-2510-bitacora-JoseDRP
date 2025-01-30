[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/RnJlnlSe)
# Bitácora Sistemas Computacionales 2025

## Unidad 1

### Solución actividad 1:

#### ¿Qué es un computador digital moderno?

Un computador digital moderno es una máquina capaz de procesar información mediante el uso de sistemas binarios donde los datos se representan en 1 y 0. Su principal función es recibir, almacenar, procesar y producir datos o información, siguiendo las instrucciones de un programa.

#### ¿Cuáles son sus partes?

Un computador digital moderno tiene varias partes clave:

**CPU (Unidad Central de Procesamiento):** Ejecuta las instrucciones y procesa los datos.

**Memoria:** Almacena datos e instrucciones; incluye la RAM (temporal) y el almacenamiento secundario (permanente).

**Dispositivos de Entrada:** Permiten al usuario interactuar con el PC (teclado, ratón, etc.).

**Dispositivos de Salida:** Muestran los resultados del procesamiento (monitor, impresora, etc.).

**Fuente de Alimentación:** Proporciona energía a todos los componentes.

**Placa Base (Motherboard):** Es donde se conectan todos los componentes.


### Solución actividad 2:

- Un programa es un conjunto de instrucciones que le indica a la computadora cómo realizar una tarea.

- El lenguaje ensamblador es un lenguaje de bajo nivel que usa abreviaciones o símbolos fáciles de entender para representar las instrucciones del lenguaje de máquina, pero aún requiere ser convertido a código binario para que la computadora lo ejecute.

- El lenguaje de máquina es el código binario que la CPU puede ejecutar directamente, pero es difícil de entender para los humanos.

### Solución actividad 3:

- PC, A y D son registros pero que tienen funciones diferentes en la CPU. PC o program counter es un registro en la CPU que guarda la dirección de la siguiente instrucción que debe ser ejecutada. D o Data es un registro utilizado para almacenar datos temporales mientras ejecutamos el programa. A o Adress es un registro que almacena direcciones de memoria, se usa para cargar datos o almacenarlos.

- La CPU utiliza el PC para saber qué instrucción ejecutar a continuación. El D se usa para almacenar datos temporales mientras ejecutamos las instrucciones. El A se utiliza para cargar y almacenar datos en la memoria.


### Solución actividad 4:

La solución para esta actividad es la siguiente:

```asm
@100
D=A
@32
M=D
```

### RETO:

#### 1. Carga en D el valor 1978.

```asm
@1978
D=A
```

#### 2. Guarda en la posición 100 de la RAM el número 69.

```asm
@69
D=A
@100
M=D
```
#### 3. Guarda en la posición 200 de la RAM el contenido de la posición 24 de la RAM

```asm
@24
D=M
@200
M=D
```

#### 4. Lee lo que hay en la posición 100 de la RAM, resta 15 y guarda el resultado en la posición 100 de la RAM.

```asm
@15
D=A
@100
M=M-D
```
#### 5. Suma el contenido de la posición 0 de la RAM, el contenido de la posición 1 de la RAM y con la constante 69. Guarda el resultado en la posición 2 de la RAM.


```asm
@0
D=M
@1
D=D+M
@69
D=D+A
@2
M=D
```

#### 6. Si el valor almacenado en D es igual a 0 salta a la posición 100 de la ROM.

```asm
@0
D=A
@100
D;JEQ
```

#### 7. Si el valor almacenado en la posición 100 de la RAM es menor a 100 salta a la posición 20 de la ROM.

```asm
@100
D=M
@100
D=D-A
@12
D;JLT
```

#### 8. Considera el siguiente programa.

- Este programa apunta a la variable 1 para luego guardar en D el valor almacenado en esa posición de la RAM. Luego apunta a la variable 2 para sumar el valor almacenado en esta variable con el valor que teníamos previamente guardado en D. Finalmente apunta a una variable 3 para almacenar el resultado de la suma previa en esta posción.

- 



