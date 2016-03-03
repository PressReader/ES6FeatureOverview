### `let` will hoist the variable to the top of the block.

However, referencing the variable in the block before the variable declaration results in a `ReferenceError`.
```JavaScript
function do_something() {
  console.log(foo); // ReferenceError
  let foo = 2;
}
```
This is called **temporal dead zone** (TDZ);
##### [`-> let in loops`](let_loops.md)
