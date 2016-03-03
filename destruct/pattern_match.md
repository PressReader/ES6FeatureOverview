### Allows binding using pattern matching
##### Supports matching arrays
```JavaScript
let foo = [1, 2, 3];
let [one, two, three] = foo;

console.log(one + two + three); // 6
```
##### and objects
```JavaScript
let o = {p: 42, q: true};
let {p, q} = o;
console.log(p); // 42
console.log(q); // true

// Assign new variable names
let {p: foo, q: bar} = o; // foo === 42, bar === true
```

##### [`-> fail safe`](fail_safe.md)
