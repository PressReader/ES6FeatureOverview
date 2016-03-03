### [Arrow functions](arrows/arrow_func.md)

### [`let` and `const`](let_const/let_and_const.md)

### [Default + Rest + Spread](default_rest_spread/def_val.md)

### [Destructuring](destruct/pattern_match.md)

### [Enhanced Object Literals](obj_literals/short_prop.md)

### [Modules](modules/modules.md)

### [Classes](classes/classes.md)

### [New built-in objects](built-ins/proimise.md)

### [[TODO]iterators + for..of](#iterators--forof)

### [[TODO]generators](#generators)

### [[TODO]template strings](#template-strings)

### Iterators + For..Of

#### Array
```JavaScript
let iterable = [1, 2, 3];

for (let value of iterable) {
  console.log(value);
}
// 1
// 2
// 3
```

#### String
```JavaScript
let iterable = "boo";

for (let value of iterable) {
  console.log(value);
}
// "b"
// "o"
// "o"
```


#### Difference between for...of and for...in
```JavaScript
let iterable = [3, 5, 7];
iterable.foo = "hello";

for (let i in iterable) {
  console.log(i); // logs 0, 1, 2, "foo"
}

for (let i of iterable) {
  console.log(i); // logs 3, 5, 7
}
```
Also about Symbols here

### Generators

### Template strings

