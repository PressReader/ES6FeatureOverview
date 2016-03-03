### New primitive type
- Immutable
- Can be used as an identifier for object properties
- Might be used to guarantee property uniqness

```JavaScript
let sym = Symbol("foo");    // name is optional
let foo = {[sym]: 42};
```

### Each call produces a new object

```JavaScript
Symbol("foo") === Symbol("foo"); // false
```

### Well-known symbols

#### Default iterator `Symbol.iterator` used in `for (... of ...)` statement

```JavaScript
var myIterable = {}
myIterable[Symbol.iterator] = function* () {
    yield 1;
    yield 2;
    yield 3;
};
[...myIterable] // [1, 2, 3]
```

##### [`-> Proxy and Reflect`](proxy_reflect.md)