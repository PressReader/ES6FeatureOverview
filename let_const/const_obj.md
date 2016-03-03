### `const` does not make the value it holds immutable, just that the variable identifier cannot be reassigned.

```JavaScript
const y = {
  count: 1,
};

y.count++;
console.log(y.count);	// prints 2
```

An initializer for a constant is required.
##### [`<<`](../README.md)
