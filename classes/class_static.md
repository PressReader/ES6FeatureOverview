### Define static method with `static`

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
> Static methods are not callable when the class is instantiated

##### [`-> subclassable Built-ins`](built_ins.md)
