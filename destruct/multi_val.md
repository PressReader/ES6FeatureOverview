### Returning multiple values
```JavaScript
function f() {
  return [1, 2];
}

let a, b;
[a, b] = f();
console.log(a, b);  // 1, 2
```
### Ignoring some returned values
```JavaScript
function f() {
  return [1, 2, 3];
}

let [a, , b] = f();
console.log(a, b);  // 1, 3
```
##### [`<<`](../README.md)