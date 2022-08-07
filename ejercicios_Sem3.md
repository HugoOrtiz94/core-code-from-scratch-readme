Lunes.
Array.prototype.length
La lengthpropiedad de un objeto que es una instancia de Arrayconjuntos de tipo o devuelve el número de elementos en esa matriz. El valor es un entero de 32 bits sin signo que siempre es numéricamente mayor que el índice más alto de la matriz.

You probably know the "like" system from Facebook and other pages. People can "like" blog posts, pictures or other items. We want to create the text that should be displayed next to such an item.

Implement the function which takes an array containing the names of people that like an item. It must return the display text as shown in the examples:

```ruby
function likes(names) {
  if (names.length == 0) return 'no one likes this';
  if (names.length == 1) return names[0] + ' likes this';
  if (names.length == 2) return names[0] + ' and ' + names[1] + ' like this';
  if (names.length == 3)
    return names[0] + ', ' + names[1] + ' and ' + names[2] + ' like this';
  return (
    names[0] +
    ', ' +
    names[1] +
    ' and ' +
    (names.length - 2) +
    ' others like this'
  );

  // TODO
}
```

Write a function that takes an integer as input, and returns the number of bits that are equal to one in the binary representation of that number. You can guarantee that input is non-negative.

Example: The binary representation of 1234 is 10011010010, so the function should return 5 in this case

```ruby
var countBits = function (n) {
  let binaryNumber = n.toString(2);
  let oneBitCount = 0;
  for (let i = 0; i < binaryNumber.length; i++) {
    if (binaryNumber[i] === '1') oneBitCount++;
  }
  return oneBitCount;
};
```

Your task is to sort a given string. Each word in the string will contain a single number. This number is the position the word should have in the result.

Note: Numbers can be from 1 to 9. So 1 will be the first word (not 0).

If the input string is empty, return an empty string. The words in the input String will only contain valid consecutive numbers.

```ruby
function getWordNumber(word) {
  for (let i = 0; i < word.length; i++) {
    if (!Number.isNaN(Number(word[i]))) return word[i];
  }
}

function cleanUndefined(array) {
  let result = [];
  for (let i = 0; i < array.length; i++) {
    if (array[i] != undefined) result.push(array[i]);
  }
  return result;
}

function order(words) {
  let sortedArray = [];
  let wordsArray = words.split(' ');
  for (let i = 0; i < wordsArray.length; i++) {
    let wordNumber = getWordNumber(wordsArray[i]);
    sortedArray[wordNumber] = wordsArray[i];
  }
  return cleanUndefined(sortedArray).join(' ');
}
```

MARTES
Move the first letter of each word to the end of it, then add "ay" to the end of the word. Leave punctuation marks untouched.

```ruby
function pigIt(str){
  //Code here
  let pMarks = ['!', '¡', '?', '¿', '.', ',', ':', ';'];
  str = str.split(' ');
  for (let i = 0; i < str.length; i++) {
    if (pMarks.indexOf(str[i]) >= 0) continue;
    str[i] = str[i].slice(1) + str[i].slice(0, 1) + 'ay';
  }
  return str.join(' ');
}
```
