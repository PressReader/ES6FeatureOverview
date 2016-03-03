Features covered in this overview:
- [arrow functions](arrows/arrow_func.md)
- [let and const](let_const/let_and_const.md)
- [destructuring](#destructuring)
- [default + rest + spread](#default--rest--spread)
- [enhanced object literals](#enhanced-object-literals)
- [iterators + for..of](#iterators--forof)
- [generators](#generators)
- [classes](#classes)
- [modules](#modules)
- [new built-in objects](#new-built-in-objects)
- [template strings](#template-strings)


### Destructuring

### Default + Rest + Spread

### Enhanced Object Literals

### Iterators + For..Of

#### Array
```JavaScript
let iterable = [1, 2, 3];

for (let value of iterable) {
  console.log(value);
}
// 1
// 2
// 3
```

#### String
```JavaScript
let iterable = "boo";

for (let value of iterable) {
  console.log(value);
}
// "b"
// "o"
// "o"
```


#### Difference between for...of and for...in
```JavaScript
let iterable = [3, 5, 7];
iterable.foo = "hello";

for (let i in iterable) {
  console.log(i); // logs 0, 1, 2, "foo"
}

for (let i of iterable) {
  console.log(i); // logs 3, 5, 7
}
```
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

