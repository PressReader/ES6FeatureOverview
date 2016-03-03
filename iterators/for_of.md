### New loop statement for custom iteration.
- Simple iterable protocol
- Enables lazy design patterns like `LINQ`

```JavaScript
function getReverseIterator(array) {
  return function() {
    let nextIndex = array.length;
    return {
      next: function() {
        return nextIndex ?
          {value: array[--nextIndex], done: false} :
          {done: true};
      }
    };
  };
}

let reverseCollection = {
  [Symbol.iterator]: getReverseIterator([1, 2, 3])
}

for(let v of reverseCollection) {
  console.log(v);
}
```

> Must use `Symbol.iterator` to hook up the iteration

> Many built-in objects like `ArrayMap`, `Set`, `String`, are iterable

##### [`-> generators`](generators.md)


