### `Promise` is used for deferred and asynchronous operations

```JavaScript
new Promise(function(resolve, reject) {
    // ...
});
```

### Static methods

> wait for all to be resolved

```JavaScript
Promise.all(iterable);
```
> wait for the first one to be resolved

```JavaScript
Promise.race(iterable)
```

> immediately resolved promise

```JavaScript
Promise.reject(reason);
```

> immediately rejected promise

```JavaScript
Promise.resolve(value)
```

##### [`-> Map, Set, WeakMap, WeakSet`](map_set.md)
