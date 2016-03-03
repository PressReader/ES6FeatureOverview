### `let` declares a block scope local variable

```JavaScript
let f = (value) => {
	let factor = 2;
	let delta = 1;

	if(value > 2) {
		let delta = 4 // different variable!
		factor += delta;
	} else {
		let factor = 5;	// different variable!
		delta += factor;
	}

	return result * factor + delta;
};
```
##### [`-> hoisting`](let_hoist.md)
