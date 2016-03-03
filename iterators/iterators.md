### Iterators are very similar to CLR `IEnumerable` or Java `Iterable`
> every `next()` call should return an object which has two fields `done` and `value`

```JavaScript
let fibonacci = {
  [Symbol.iterator]() {
    let pre = 0, cur = 1;
    return {
      next() {
        [pre, cur] = [cur, pre + cur];
        return { done: false, value: cur }
      }
    }
  }
}

for (var n of fibonacci) {
  if (n > 1000) {
    break;
  }
  console.log(n);
}
```

##### [`-> for..of`](for_of.md)


