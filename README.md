Features covered in this overview:
- [arrow functions](#arrow-functions)
- [let and const](#let-and-const)
- [destructuring](#destructuring)
- [default + rest + spread](#default--rest--spread)
- [enhanced object literals](#enhanced-object-literals)
- [iterators + for..of](#iterators--forof)
- [generators](#generators)
- [classes](#classes)
- [modules](#modules)
- [new built-in objects](#new-built-in-objects)
- [template strings](#template-strings)


### Arrow functions
Function shorthand using `=>` syntax.
Syntactically similar to the related feature in C# of Java.

Function body can be an expression:
```JavaScript
var inc = arr.map(v => v + 1);
var inc = arr.map((value, index) => v + i);	// equivalent to: (value, index) => { return v + i; }
```

Or statement:
```JavaScript
var filterEven = (filtered, val) => {
	if(val % 2 === 0) {
		filtered.push(val);
	}
};
```

`this` is always taken from lexical scope.
```JavaScript
var preson = {
	_name: 'Bob Ross',
	_friendsCount: 9999,
	addFriend () {
		setTimeout(() => {
			this._friendsCount++;
			console.log(this._name, 'has', this._friendsCount, 'friends!');
		}, 200);
	}
};
```

Since an arrow function is always bound to the context, "use strict" instruction is just ignored
```JavaScript
var f = () => {'use strict'; return this; };
f() === window; // or another global object
```

`call` or `apply`, has no effect, only arguments can be passed.
```JavaScript
var f = (a,b) => {
	console.log('context', this);
	console.log('first arg', a);
	console.log('second arg', a);
};

f.call({name: 'Bob'}, 1, 2);
```

Use concise syntax when return object literal
The code inside braces ({}) is parsed as a sequence of statements
(i.e. foo is treated like a label, not a key in an object literal).
```JavaScript
var f = () => {  foo: 1  };               // Calling func() returns undefined!
var f = () => {  foo: function() {}  };   // SyntaxError: function statement requires a name

//Remember to wrap the object literal in parentheses:
var f = () => ({  foo: 1  });
```

### `let` and `const`
`let` declares a block scope local variable
```JavaScript
let f = (value) => {
	let delta = 1;
	if(value > 2) {
		let factor = 2;
		return value * factor + delta;
	} else {
		let factor = 5;	// different variable!
		return value * factor;
	}
};
```
`let` will hoist the variable to the top of the block,
However, referencing the variable in the block before the variable declaration results in a `ReferenceError`.
Called Temporal Dead Zone (TDZ);
```JavaScript
function do_something() {
  console.log(foo); // ReferenceError
  let foo = 2;
}
```

`let` can be used to declare variables in the scope of the loops
```JavaScript
var i = 0;
for (let i = i; i < 10; i++) {
  console.log(i);
}
```

`const` is single-assignment. It does not mean the value it holds is immutable,
just that the variable identifier cannot be reassigned.
An initializer for a constant is required.
```JavaScript
const x = 1;
x = 2;
console.log(x); // prints 1

const y = {
	count: 1,
};
y.count++;

console.log(y.count);	// prints 2
```

### Destructuring

### Default + Rest + Spread

### Enhanced Object Literals

### Iterators + For..Of
Also about Symbols here

### Generators

### Classes
> Syntactical sugar over JavaScript's existing prototype-based inheritance.

> Does not introduce a new object-oriented inheritance model.

```JavaScript
class Person {
  constructor (name) {
    this._name = name;
  }

  // property definiton shorthand
  get name() {
    return this._name;
  }
  set name(value) {
    this._name = value;
  }

  // note that this is a prototype method
  doWork() {
    return this.name + ' is working';
  }
}
```

> Sub classing with `extends`

```JavaScript
class Employee extends Person {
  constructor (name, title) {
    super(name);	// calling base class constructor

    this._title = title;
  }

  get title() {
    return this._title;
  }

  doWork() {
    return super.doWork() + ' hard';	// calling base class method
  }
}

let greatPerson = new Person("Bob Ross");
let humblePerson = new Employee("Oleg", "developer");

for(let person of [greatPerson, humblePerson]) {
  console.log(person.doWork());
}
```

> Can also have static methods

```JavaScript
class Point {
    constructor(x, y) {
        this.x = x;
        this.y = y;
    }

    static distance(a, b) {
        let dx = a.x - b.x;
        let dy = a.y - b.y;

        return Math.sqrt(dx*dx + dy*dy);
    }
}
let p1 = new Point(5, 5);
let p2 = new Point(10, 10);

// p1.distance is not defined.

console.log(Point.distance(p1, p2));
```

###### [TODO] Subclassable Built-ins


### Modules
Aslo about module loaders here

### New built-in objects
Map, Set, WeakMap, WeakSet, Promise, Proxy

### Template strings

