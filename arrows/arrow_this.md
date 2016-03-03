### `this` is always taken from lexical scope

> Say goodbye to `.bind(this)`

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

### Arrow function is always bound to a context, `'use strict'` is just ignored

```JavaScript
var f = () => {'use strict'; return this; };
f() === window; // or another global object
```

### `call` or `apply`, has no effect, only arguments can be passed

```JavaScript
var f = (a, b) => {
	console.log('first arg', a);
	console.log('second arg', a);
	console.log(this.name);	// Error in strict mode
};

f.call({name: 'Bob'}, 1, 2);    // undefined, 1, 2
```
##### [`-> returning object literal`](arrow_obj_literal.md)
