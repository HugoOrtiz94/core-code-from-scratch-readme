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



