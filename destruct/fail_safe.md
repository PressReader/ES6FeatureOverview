### Destructuring is fail-safe, similar to standard object lookup
```JavaScript
let [foo] = [];
console.log(foo === undefined);   // true
```
### Or can be used with default value
```JavaScript
let [bar = 1] = [];
console.log(bar === 1);   // true
```
##### [`-> even more flexibility`](multi_val.md)
