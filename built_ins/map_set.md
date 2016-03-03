### Efficient data structures for common algorithms

#### Map

```JavaScript
let m = new Map();
m.set("hello", 42);

let s = {};
m.set(s, 34);
m.get(s) === 34;
```

#### Set

```JavaScript
let s = new Set();
s.add("hello").add("goodbye").add("hello");
s.size === 2;
s.has("hello") === true;
```

#### Entries in `Weak*` objects are weakly referenced

>The keys in `WeakMap` must be objects

> If there are no other strong references to the key, then the entry will be removed from by the garbage collector.

> `Weak*` objects are not enumerable

##### [`-> Symbol`](symbol.md)
