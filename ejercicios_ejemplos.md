

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

Cree un programa que agregue dos números proporcionados por el usuario

.data
	      number1: .asciiz "\nIngrese el primer numero: "
	      number2: .asciiz "\nIngrese el segundo numero: "
  .text
	      main:
              li $v0, 4
              la $a0, number1
              syscall

              li $v0, 5
              syscall

              move $t0, $v0

              li $v0, 4
              la $a0, number2
              syscall

              li $v0, 5
              syscall

              move $t1, $v0

              li $v0, 1
              move $a0, $t0
              syscall

Crea un programa que muestre tu nombre

.data
        message: .asciiz "\nMi nombre es Hugo Leonel Ortiz\n"
  .text
        main:
              li $v0, 4
              la $a0, message
              syscall
#JUEVES
1. Print special numbers exercise
```for (var i = 0; i <= 100; i++) {
  if (i % 2 == 0) console.log(i);
}
```var i = 0;
while (i <= 100) {
  if (i % 2 == 0) console.log(i);
  i++;
}
```var i = 0;
while (i <= 100) {
  if (i % 2 == 0) console.log(i);
  i++;
}

2. Bad Code exercise
El código que se muestra a continuación no está funcionando de la manera correcta, como tarea debes encontrar el error que cometió el desarrollador que programó este código y corregirlo, para este ejercicio debes explicar cuál es el error y colocar el código correcto

```var cond = false;

if ((cond = true)) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}

Solucion

```var cond = false;

if (cond) {
  console.log('The cond variable is true');
} else {
  console.log('The cond variable is false');
}





3. mal código 2

var n = 100;

if (n == 100) {
  console.log('This is a special number!');
}
if (n < 1000) {
  console.log('');
} else {
  console.log('Just a regular number');
}
if (n % 10 == 0) {
  console.log('This number is multiple of 10');
}

Solución

var n = 100;

if (n == 100) {
  console.log('This is a special number!');
} else if (n < 1000 && n % 10 == 0) {
  console.log('This number is almost special');
} else {
  console.log('Just a regular number');
}




