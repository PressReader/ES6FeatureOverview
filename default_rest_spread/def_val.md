### Function arguments can have default values
```JavaScript
function f(x, y = 12) {
  return x + y;
}

f(3);    // 15
```
### Nested defaults also available
```JavaScript
function drawChart({size = 'big', cords = { x: 0, y: 0 }, radius = 25} = {}) {
  console.log(size, cords, radius);
}

drawChart({
  cords: { x: 18, y: 30 }
});
```
##### [`-> rest`](rest.md)