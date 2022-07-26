if...else
The if statement executes a statement if a specified condition is truthy. If the condition is falsy, another statement in the optional else clause will be executed.

Try it

```function testNum(a) {
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

......


