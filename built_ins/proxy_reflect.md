### `Proxy` is used to define custom behavior for fundamental operations (e.g. property lookup, assignment, enumeration, function invocation, etc).

```JavaScript
var handler = {
    get: function(target, name) {
        return name in target?
            target[name] :
            42;
    }
};

var foo = new Proxy({}, handler);
foo.bar = 1;
console.log(foo.bar, foo.buzz); // 1, 42
```
> Proxy getters, setters, constructors, property deleting, enumeration and so much more!

### `Reflect` provides methods for interceptable JavaScript operations.
##### Invoke constructor

```JavaScript
let d = Reflect.construct(Date, [1776, 6, 4]);
d instanceof Date; // true
d.getFullYear(); // 1776
```

#### Call a function

```JavaScript
Reflect.apply(Math.floor, undefined, [1.75]); // 1
```
> The methods of `Reflect` object are the same as those of `Proxy`.

##### [`<<`](../README.md)
