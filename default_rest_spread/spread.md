### Allows an expression to be expanded in places where multiple arguments or multiple elements are expected

##### In function calls
```JavaScript
function f(x, y, z) { }
let args = [0, 1, 2];
f(...args); // equals to f(0, 1, 2);
```
> Better `.push`

```JavaScript
let arr1 = [0, 1, 2];
let arr2 = [3, 4, 5];
arr1.push(...arr2);
```
##### In array literals
```JavaScript
let [a, b, ...iterable] = [1, 2, 3, 4, 5];
console.log(iterable.join());   // 3, 4, 5
```
> Even more poweful!

```JavaScript
let arr = [1, 2];
let extended = [0, ...arr, 3, 4];   // [0, 1, 2, 3, 4]
```
##### [`<<`](../README.md)