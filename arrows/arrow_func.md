  ### Arrow functions
> Function shorthand using `=>` syntax

> Syntactically similar to the related feature in C# of Java

```JavaScript
//Function body can be an expression
var inc = arr.map(v => v + 1);
var inc = arr.map((value, index) => v + i);	// equivalent to: (value, index) => { return v + i; }

//Or statement:
var filterEven = (filtered, val) => {
	if(val % 2 === 0) {
		filtered.push(val);
	}
};
```
