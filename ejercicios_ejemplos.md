

##MARTES

Interpreted And Compiled Programming Languages

En un lenguaje compilado, la máquina de destino traduce directamente el programa. En un idioma interpretado, el código fuente no es traducido directamente por la máquina de destino. En cambio, un programa diferente , también conocido como el intérprete, lee y ejecuta el código.


¿Java está compilado o interpretado, o ambos?

*/Sí, un programa Java primero se compila en un código de bytes que JRE puede entender. ByteCode luego es interpretado por la JVM convirtiéndolo en un lenguaje interpretado./*

Pseudocode currency converter

Descripción
Has sido seleccionado para desarrollar el algoritmo que se utilizará para convertir dólares (USD) a bitcoin (BTC), para ello lo primero que debes hacer es entregar un pseudocódigo con el algoritmo a desarrollar, de esta forma podrás explicarlo en una mejor manera para el equipo lo que será la operación requerida. La idea principal es tener un sitio web donde se le pedirá al usuario que ingrese la cantidad a convertir.

Pasos. 
1. Inicio.
2. Solicitar cantidad dolares
3. solicitar valor de bitcoin
4. Realizar convercion ($cantidad dolares * Valor bitcoin)
5. resultado
6. fin

High and Low level languages


EL nivel indica la cantidad de abstracción entre el lenguaje de programación y el lenguaje de maquina que es un conjunto de instrucciones ejecutadas directamente desde la CPU y es el unico lenguaje que una computadora es capaz de entender


###MIERCOLES

1. ¿Tu fecha de nacimiento en la matriz? ejercicio
BASE
20 = 1
21 = 2
22 = 4
23 = 8
24 = 16
25 = 32
26 = 64
27 = 128
28 = 256
29 = 512
210 = 1024
211 = 2048
2^10	2^9	2^8	2^7	2^6	2^5	2^4	2^3	2^2	2^1	2^0
1	1	1	1	1	0	0	1	0	1	1

Adjunto respuesta
11 de Diciembre de 1994
11 = 8, 2, 1
     1 1 1
12 = 8 4 
     1 0
1994= 1024, 512, 256, 128, 64, 8, 2

       1 1 1 1 1 1 1

Respuesta formato 11/12/1994:
111/10/111111



#2. ejercicio MIPS

Ejemplo:

.data
        message: .asciiz "\nHello, World!\n"
  .text
        main:
              li $v0, 4
              la $a0, message
              syscall
