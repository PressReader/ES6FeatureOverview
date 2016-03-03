### Represents an indefinite number of arguments as an array.

> say goodbye to `arguments`

```JavaScript
function sortArgs(...theArgs) {
  let sortedArgs = theArgs.sort();
  return sortedArgs;
}

console.log(sortArgs(5,3,7,1)); // [1, 3, 5, 7]
```

### Take as many arguments as needed
```JavaScript
function multiply(multiplier, ...args) {
  return args.map(e => multiplier * e);
}

console.log(multiply(2, 1, 2, 3)); // [2, 4, 6]
```
##### [`-> spread`](spread.md)