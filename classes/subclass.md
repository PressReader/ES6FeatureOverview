### Sub classing with `extends`

> Base class is accessible with `super`


```JavaScript
class Employee extends Person {
  constructor (name, title) {
    super(name);  // calling base class constructor

    this._title = title;
  }

  get title() {
    return this._title;
  }

  doWork() {
    return super.doWork() + ' hard';  // calling base class method
  }
}

let greatPerson = new Person("Bob Ross");
let humblePerson = new Employee("Oleg", "developer");

for(let person of [greatPerson, humblePerson]) {
  console.log(person.doWork());
}
```

##### [`-> static methods`](class_static.md)
