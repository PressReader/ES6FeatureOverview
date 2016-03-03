### Computed method names

```JavaScript
let buzz = {
   [ 'fo' + (() => 'o')() ]: 42
};
console.log(buzz.foo)	// 42
```

### Shorthand generators

```JavaScript
let buzz = {
   * generator() {}
};
```


##### [`<<`](../README.md)


