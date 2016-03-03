### Syntactical sugar over JavaScript's existing prototype-based inheritance.

> Does not introduce a new object-oriented inheritance model

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

> Class declarations and class expressions are executed in `strict mode`

> Unlike function declarations, class declaration are not hoisted

##### [`-> sub classing`](subclass.md)
