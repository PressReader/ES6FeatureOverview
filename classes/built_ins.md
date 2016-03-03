### Built-in objects like `Array`, `Date`, `Error` can be subclassed.
```JavaScript
class MyArray extends Array {
    constructor(...args) {
        super(...args);
    }
}

let myArr = new MyArray();
myArr[0] = 'foo';
console.log(myArr.length); // 1
```
##### [`<<`](../README.md)