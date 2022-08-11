
replace, solo lee de izquierda a derecha
```ruby
let str = 'hello'
let charBackup = 'e';
str = str.replace(str[0], str.charCodeAT(0));
str = str.replace (charBackup, str [str.length-1]);
str = str.replace(/
console.log(str);

```
//MDM diccionario de javascript para buscar lo que hace cada funcionm
TAREA resolver el ejercicio.

Cambiar de posición.
// [hello, world]

```ruby
let str = 'world';
let charBackup = str[1];

// 1
/*
  W0[0].charCodeAt(0) 
*/
str = str.replace(str[0], str.charCodeAt(0));

// 2
/*
 W0[1] = W0[W0.length-1]
 W0[W0.length-1] = W0[1]
*/
str = str.replace(charBackup, str[str.length-1]);
str = str.replace(/\w$/, charBackup);

//str = str.slice(0, str.length-1) + charBackup;
//str = `${str.slice(0, str.length-1)}${charBackup}`;
//str = str.slice(0, str.length-1).concat(charBackup);

console.log(str); //104olle

```


#Leccion de como filtrar una matriz --filter--

```ruby
const numbers = [1, -1, 2, 3];
const filtered = numbers.filter(function(value) {
	return value>=0;
});
console.log(filtered) //[1,2,3]

```

#array reduce

```ruby
const numbers = [1, -1, 2, 3];
*/para no hacer todo esto se reduce:
let sum = 0;
for (let n of numbers)
	sum += n;

console.log(sum);
*/


const sum = numbers.reduce(
	(accomulator, currentValue) => accumulator + currentValue
);
console.log(sum);


```
#Javascript Array Map


```ruby
const numbers = [1, -1, 2, 3];

const items = numbers
	.filter(n => n >= 0)
	.map(n => ({ value: n}))
	.filter(obj => obj.value > 1);
console.log(items);

```

#Regular Expressions (RegEx) 

```ruby
const regex = /bob/gimsy

```


#String.replace

```ruby
const mStr = "Hey, I'm 25 and she's 31!";

	console.log(myStr.replace(/(\d+)([^\d]+)(\d+)/g. function(match. g1, g2, g3) {
		return parseInt(g1) + parseInt(g3);
}));

```
