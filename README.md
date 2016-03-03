Features covered in this overview:
- # [Arrow functions](arrows/arrow_func.md)
- # [`let` and `const`](let_const/let_and_const.md)
- # [default + rest + spread](default_rest_spread/def_val.md)
- # [destructuring](destruct/pattern_match.md)
- # [[TODO]enhanced object literals](#enhanced-object-literals)
- # [[TODO]modules](#modules)
- # [classes](classes/classes.md)
- # [[TODO]new built-in objects](#new-built-in-objects)
- # [[TODO]iterators + for..of](#iterators--forof)
- # [[TODO]generators](#generators)
- # [[TODO]template strings](#template-strings)


### Enhanced Object Literals

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

### Modules
Aslo about module loaders here

### New built-in objects
Map, Set, WeakMap, WeakSet, Promise, Proxy

### Template strings

