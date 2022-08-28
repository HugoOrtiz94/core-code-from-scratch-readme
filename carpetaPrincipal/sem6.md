 #Typescript

** Introduction to Object Oriented Programming
* $Abstraction
* $Inheritance
* $Polymorphism
* $Encapsulation
* $Concept of class
* $Attributes
* $Methods
* $Constructor
* $Classes with Typescript
* $Concept of instance

Boolean type
The most basic datatype is the true or false value, known as a boolean.

For example:

```
let flag: boolean;
let yes = true;
let no = false;
```

Number and BigInteger types
```
let x: number;
let y = 0;
let z: number = 123.456;
let big: bigint = 100n;
```

La stringpalabra clave representa secuencias de caracteres almacenados como unidades de código Unicode UTF-16. Al igual que JavaScript, TypeScript también usa comillas dobles ( ") o comillas simples ( ') para rodear datos de cadena.
```
let s: string;
let empty = "";
let abc = 'abc';
```

Ejercicio - enumeraciones
```
enum ContractStatus {
     Permanent = 1,
     Temp,
     Apprentice
}

let employeeStatus: ContractStatus = ContractStatus.Temp;
console.log(employeeStatus);

console.log(ContractStatus[employeeStatus]);
```

Cualquier tipo
El anytipo es el tipo que puede representar cualquier valor de JavaScript sin restricciones. Esto puede ser útil cuando espera un valor de una biblioteca de terceros o entradas de usuario donde el valor es dinámico porque el anytipo le permitirá reasignar diferentes tipos de valores. Y, como se mencionó anteriormente, usar el anytipo le permite migrar gradualmente su código JavaScript para usar tipos estáticos en TypeScript.

El siguiente ejemplo declara una variable de tipo anyy le asigna valores:
```
let randomValue: any = 10;
randomValue = 'Mateo';   // OK
randomValue = true;      // OK
```
tipo desconocido
Si bien es flexible, el anytipo puede causar errores inesperados. Para abordar esto, TypeScript introdujo el unknowntipo.

El unknowntipo es similar al anytipo en que se puede asignar cualquier valor al tipo unknown. Sin embargo, no puede acceder a ninguna propiedad de un unknowntipo, ni puede llamarlas o construirlas.

Este ejemplo cambia el anytipo del ejemplo anterior a unknown. Ahora generará errores de verificación de tipos y le impedirá compilar el código hasta que tome las medidas adecuadas para resolverlos.

```
let randomValue: unknown = 10;
randomValue = true;
randomValue = 'Mateo';

console.log(randomValue.name);  // Error: Object is of type unknown
randomValue();                  // Error: Object is of type unknown
randomValue.toUpperCase();      // Error: Object is of type unknown
```

 Nota

La principal diferencia entre anyy unknownes que no puede interactuar con una variable de tipo unknown; hacerlo genera un error de compilación . anyomite cualquier verificación en tiempo de compilación y el objeto se evalúa en tiempo de ejecución; si el método o la propiedad existe, se comportará como se esperaba.

