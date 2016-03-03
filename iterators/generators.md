### Generators are functional-style iterators

> Generator function returns `Generator` object

> New keyword `yield`

```JavaScript
var markers = {
  [Symbol.iterator]: function* () {
    var index = 0;
    while(index < 3)
      yield index++;
    }
  }

for (var m of markers) {
  console.log(m);
}
```

> Generators are not constructable

##### [`<<`](../README.md)


