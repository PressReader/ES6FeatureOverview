### Shorthand methods

```JavaScript
let buzz = {
  foo(...args) {
    return args.join(':');
  }
};

console.log(buzz.foo(1, 2, 3)); // 1:2:3
```
##### [`-> some more`](misc.md)
