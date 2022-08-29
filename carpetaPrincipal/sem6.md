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

La principal diferencia entre any y unknownes que no puede interactuar con una variable de tipo unknown; hacerlo genera un error de compilación . anyomite cualquier verificación en tiempo de compilación y el objeto se evalúa en tiempo de ejecución; si el método o la propiedad existe, se comportará como se esperaba.

Tipos de unión
Un tipo de unión describe un valor que puede ser uno de varios tipos. Esto puede ser útil cuando un valor no está bajo su control (por ejemplo, valores de una biblioteca, una API o entrada del usuario).

El anytipo también puede aceptar diferentes tipos, entonces, ¿por qué querría usar un tipo de unión? Los tipos de unión restringen la asignación de valores a los tipos especificados, mientras que cualquier tipo no tiene restricciones. Otra razón es el soporte de Intellisense.

Un tipo de unión usa la barra vertical o tubería ( |) para separar cada tipo. En el siguiente ejemplo, multiTypepuede ser a  numbero a  boolean:
```
let multiType: number | boolean;
multiType = 20;         //* Valid
multiType = true;       //* Valid
multiType = "twenty";   //* Invalid
```

 la addfunción acepta dos valores que pueden ser a numbero a string.
 Si ambos valores son tipos de números, los suma. Si ambos son tipos de cadena, los concatena. De lo contrario, genera un error.
 ```
 function add(x: number | string, y: number | string) {
    if (typeof x === 'number' && typeof y === 'number') {
        return x + y;
    }
    if (typeof x === 'string' && typeof y === 'string') {
        return x.concat(y);
    }
    throw new Error('Parameters must be numbers or strings');
}
console.log(add('one', 'two'));  //* Returns "onetwo"
console.log(add(1, 2));          //* Returns 3
console.log(add('one', 2));      //* Returns error
```
 El siguiente ejemplo define dos interfaces, Employeey Manager, y luego crea un nuevo tipo de intersección llamado ManagementEmployeeque combina las propiedades en ambas interfaces.
 
```
 interface Employee {
  employeeID: number;
  age: number;
}
interface Manager {
  stockPlan: boolean;
}
type ManagementEmployee = Employee & Manager;
let newManager: ManagementEmployee = {
    employeeID: 12345,
    age: 34,
    stockPlan: true
};
```
Por el contrario, usar constpara declarar una variable informará a TypeScript que este objeto nunca cambiará. Declarándolo con consttipos al valor (por ejemplo, "Hello World").

arreglos
TypeScript, como JavaScript, le permite trabajar con matrices. Los arreglos se pueden escribir de una de dos maneras. En el primero, usa el tipo de los elementos seguido de corchetes ( [ ]) para indicar una matriz de ese tipo de elemento:
```
let list: number[] = [1, 2, 3];
```
**La segunda forma usa un tipo genérico Array, usando la sintaxis Array<type>:**
```
let list: Array<number> = [1, 2, 3];
```

Abra el archivo module02.ts y localice el Ejercicio 1 .
 
/* Module 2: Declare variable types in TypeScript
   Lab start  */

/*  EXERCISE 1
    TODO: Modify the code to add types to the variable declarations. 
    The resulting JavaScript should look the same as the original example when you're done. */
```
let firstName: string;
let lastName: string;
let fullName: string;
let age: number;
let ukCitizen: boolean;

firstName = "Rebecca";
lastName = "Smith";
age = 42;
ukCitizen = false;
fullName = firstName + " " + lastName;

if (ukCitizen) {
  console.log(
    "My name is " +
      fullName +
      ", I'm " +
      age +
      ", and I'm a citizen of the United Kingdom."
  );
} else {
  console.log(
    "My name is " +
      fullName +
      ", I'm " +
      age +
      ", and I'm not a citizen of the United Kingdom."
  );
}
```
/* EXERCISE 2
   TODO: You can use types to ensure operation outcomes. Run the code as is and then modify 
   it to have strongly typed variables. Then, address any errors you find so that the result 
   returned to a is 12. */
```
let x: number;
let y: number;
let a: number;

x = 5;
y = 7;
a = x + y;

console.log(a);
```
/* EXERCISE 3
   TODO: In the following code, implement an enum type called Season that represents 
   the constants "Fall", "Winter", "Spring", and "Summer". Then, update the function so 
   you can pass in the season by referencing an item in the enum, for example 
```   
Season.Fall, instead of the literal string "Fall". */
enum Season {
  Winter,
  Spring,
  Summer,
  Fall
}

function whichMonths(season: Season) {

  let monthsInSeason: string;

  switch (season) {
    case Season.Fall:
      monthsInSeason = "September to November";
      break;
    case Season.Winter:
      monthsInSeason = "December to February";
      break;
    case Season.Spring:
      monthsInSeason = "March to May";
      break;
    case Season.Summer:
      monthsInSeason = "June to August";
  }

  return monthsInSeason;
}

console.log(whichMonths(Season.Spring));
```
/* EXERCISE 4
   TODO: Declare the array as the type to match the type of the items in the array. */
```
let randomNumbers: number[] = [];
let nextNumber: number;

for (let i = 0; i < 10; i++) {
    nextNumber = Math.floor(Math.random() * (100 - 1)) + 1;
    randomNumbers.push(nextNumber);
}

console.log(randomNumbers);
```
Exercise:

    Given the data, define the interface "User" and use it accordingly.
```
*/
export type User = {
name: string;
age: number;
occupation: string;
}

export const users: User[] = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    }
];

export function logPerson(user: User) {
    console.log(` - ${user.name}, ${user.age}`);
}

console.log('Users:');
users.forEach(logPerson);
```                       
                       
Exercise:

    Type "Person" is missing, please define it and use
    it in persons array and logPerson function in order to fix
    all the TS errors.
                       
 ```
 interface User {
    name: string;
    age: number;
    occupation: string;
}

interface Admin {
    name: string;
    age: number;
    role: string;
}

export type Person = User | Admin;

export const persons: Person[] /* <- Person[] */ = [
    {
        name: 'Max Mustermann',
        age: 25,
        occupation: 'Chimney sweep'
    },
    {
        name: 'Jane Doe',
        age: 32,
        role: 'Administrator'
    },
    {
        name: 'Kate Müller',
        age: 23,
        occupation: 'Astronaut'
    },
    {
        name: 'Bruce Willis',
        age: 64,
        role: 'World saver'
    }
];

export function logPerson(user: Person) {
    console.log(` - ${user.name}, ${user.age}`);
}
console.log('Users: ')
persons.forEach(logPerson);                   
```
