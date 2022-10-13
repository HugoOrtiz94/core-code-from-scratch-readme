##Object-Oriented Programming - Resume
La programación orientada a objetos es un paradigma de programación basado en la creación de objetos que pueden contener datos y funciones.

Se dice que la programación orientada a objetos busca que representemos nuestro código y algoritmos con objetos, como en la vida real.

Este paradigma está basado, principalmente en los principios de abstracción, encapsulación o encapsulamiento, herencia y polimorfismo

TypeScript agrega algunas capacidades nuevas a las funciones estándar de JavaScript para que sea más fácil trabajar con ellas.

Esta función acepta dos parámetros de tipo numbery devuelve un number.
```
}function addNumbers (x: number, y: number): number {
   return x + y;
}
addNumbers(1, 2);
```

1. ¿Cuál es la diferencia entre los parámetros de función en TypeScript y los parámetros de función en JavaScript?

Los parámetros de TypeScript son obligatorios de forma predeterminada, pero se pueden hacer opcionales. Los parámetros de JavaScript son siempre opcionales.

2. .¿Cuál es un uso común para una función anónima?
Cuando necesite asignar una expresión de función a una variable.

3.¿Cómo debe definir un tipo de función si necesita extenderlo?

Defínalo con una interfaz.


Ejemplo de clase abstracta 1
En este primer ejemplo, la clase abstracta Animaltiene una propiedad abstracta name. Gato y Perro deben implementar la propiedad nameellos mismos en lugar de heredar de la clase base.

Tenga en cuenta que abstract nameen la Animaldefinición de clase no se puede inicializar un valor ni en la definición de atributo de clase ni en su constructor. Ahora es una regla que indica que namela clase derivada debe inicializarla.

```
abstract class Animal {
    abstract name: string
    age: number

    constructor(age: number) {
        //this.name = name // this must now be assigned in the derived class instead
        this.age = age
    }

    feed(food: string, amount: number): void {
        console.log(
            'Feeding ' +
                this.name +
                ' the ' +
                this.constructor.name +
                ' ' +
                amount +
                ' kg of ' +
                food
        )
    }
}

class Cat extends Animal {
    name: string
    constructor(name: string, age: number) {
        super(age)
        this.name = name
    }
}

class Dog extends Animal {
    name: string
    constructor(name: string, age: number) {
        super(age)
        this.name = name
    }
}

const CAT = new Cat('Cosmo', 8)
const DOG = new Dog('Rusty', 12)
CAT.feed('Fish', 0.1)
DOG.feed('Beef', 0.25)
```

Clases abstractas vs interfaces

Una clase abstracta es practicamente identica a una clase convencional; las clases abstractas pueden poseer atributos, métodos, constructores, etc ... La principal diferencia entre una clases convencional y una clase abstracta es que la clase abstracta debe poseer por lo menos un método abstracto. Ok, pero ahora, ¿ Qué es un método abstracto? Verás, un método abstracto no es más que un método vacío, un método el cual no posee cuerpo, por ende no puede realizar ninguna acción. La utilidad de un método abstracto es definir qué se debe hacer pero no el cómo se debe hacer.

Podemos definir a una interfaz como una colección de métodos abstractos y propiedades constantes en las que se especifica que se debe de hacer pero no como, serán las clases hijas quienes definan el comportamiento.

#Miercoles

Array.prototype.forEach()
El forEach()método ejecuta una función proporcionada una vez para cada elemento de la matriz.
```
const array1 = ['a', 'b', 'c'];

array1.forEach(element => console.log(element));

// expected output: "a"
// expected output: "b"
// expected output: "c"
```

Matemáticas.pow()
El Math.pow()método devuelve el valor de una base elevada a una potencia. Eso es

𝙼𝚊𝚝𝚑.𝚙𝚘𝚠 ( 𝚡 , 𝚢 ) = X y
```
console.log(Math.pow(7, 3));
// expected output: 343

console.log(Math.pow(4, 0.5));
// expected output: 2

console.log(Math.pow(7, -2));
// expected output: 0.02040816326530612
//                  (1/49)

console.log(Math.pow(-7, 0.5));
// expected output: NaN
```
Escriba un analizador simple que analice y ejecute Deadfish.

Deadfish tiene 4 comandos, cada uno de 1 carácter:

iincrementa el valor (inicialmente 0)
ddisminuye el valor
seleva al cuadrado el valor
ogenera el valor en la matriz de retorno
Los caracteres no válidos deben ignorarse.

parse("iiisdoso") => [8, 64]
```
/** return the output array and ignore all non-op characters */
export function parse(data: string): number[] {
let value = 0;
  const result: number[] = [];
  const commands = data.split('');
  commands.forEach((command: string) => {
    switch (command) {
      case 'i':
        value++;
        break;
      case 'd':
        value--;
        break;
      case 's':
        value = Math.pow(value, 2);
        break;
      case 'o':
        result.push(value);
        break;
    }
  });
  return result;  
```



#filter()
```
const words = ['spray', 'limit', 'elite', 'exuberant', 'destruction', 'present'];

const result = words.filter(word => word.length > 6);

console.log(result);
// expected output: Array ["exuberant", "destruction", "present"]
```

Duplicate Encoder
```
const appereances = (word: string[], charToCount: string) => {
  return word.filter((char: string) => char === charToCount).length;
}
export function duplicateEncode(word: string){
    // ...
  let result = '',
    encodeChar = '';
  const characters = [...word.toLowerCase()];
  characters.forEach((char) => {
    encodeChar = ')';
    if (appereances(characters, char) === 1) {
      encodeChar = '(';
    }
    result += encodeChar;
  });
  return result;
}
```

Find The Odd Int

```
const appereances = (numbers: number[], nToCount: number) => {
  return numbers.filter((n: number) => n === nToCount).length;
};

export const findOdd = (xs: number[]): number => {
  const nonRepeatNumbers = new Set(xs);
  for (let n of nonRepeatNumbers) {
    if (appereances(xs, n) % 2 !== 0) return n;
  }
  return -1;
};
```

