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



