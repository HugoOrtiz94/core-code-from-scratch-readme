**LUNES**

*if...else*
The if statement executes a statement if a specified condition is truthy. If the condition is falsy, another statement in the optional else clause will be executed.


Try it

```ruby
function testNum(a) {
  let result;
  if (a > 0) {
    result = 'positive';
  } else {
    result = 'NOT positive';
  }
  return result;
}


console.log(testNum(-5));
// expected output: "NOT positive"
```



**for**

The for statement creates a loop that consists of three optional expressions, enclosed in parentheses and separated by semicolons, followed by a statement (usually a block statement) to be executed in the loop.
JavaScript Demo: Statement - For

```ruby
let str = '';

for (let i = 0; i < 9; i++) {
  str = str + i;
}

console.log(str);
// expected output: "012345678"
```

function declaration
The function declaration (function statement) defines a function with the specified parameters.

You can also define functions using the Function constructor and a function expression.
```ruby

function calcRectArea(width, height) {
  return width * height;
}

console.log(calcRectArea(5, 6));
// expected output: 30
```

declaración de función
La declaración de función (instrucción de función) define una función con los parámetros especificados.

También puede definir funciones utilizando el Functionconstructor y una expresión de función .

```Ruby
function calcRectArea(width, height) {
  return width * height;
}

console.log(calcRectArea(5, 6));
// expected output: 30
```

Descripción
Una función creada con una declaración de función es un Functionobjeto y tiene todas las propiedades, métodos y comportamiento de los Functionobjetos. Consulte Functionpara obtener información detallada sobre las funciones.

También se puede crear una función usando una expresión (ver expresión de función ).

De forma predeterminada, las funciones devuelven undefined. Para devolver cualquier otro valor, la función debe tener una returndeclaración que especifique el valor a devolver.


**MARTES**


Multiplicación (*)
El operador de multiplicación ( *) produce el producto de los operandos.

```Ruby
num = '4 ';
num2 = '7 ';
console.log(num * num2);
```

 "Cómo convertir caracteres en javascript de número ascii"
 
 function uniTotal(str) {
  let total = 0;
  for (let i = 0, length = str.length; i < length; i++) {
    total += str[i].charCodeAt();
  }
  return total;
}



Miercoles

```Ruby
function testNum(a) {
  let result;
  if (a > 0) {
    result = 'positive';
  } else {
    result = 'NOT positive';
  }
  return result;
}

console.log(testNum(-5));
// expected output: "NOT positive"
```

Multiple if...else statements can be nested to create an else if clause. Note that there is no elseif (in one word) keyword in JavaScript.


In general, it is a good practice to always use block statements, especially in code involving nested if statements.
```Ruby
function checkValue(a, b) {
  if (a === 1) {
    if (b === 2) {
      console.log("a is 1 and b is 2");
    } else {
      console.log("a is not 1");
    }
  }
}

console.log(checkValue(-5));
```



