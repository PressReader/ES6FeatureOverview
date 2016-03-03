### Use concise syntax when returning object literal

```JavaScript
var f = () => {  foo: 1  };               // Calling func() returns undefined!
var f = () => {  foo: function() {}  };   // SyntaxError: function statement requires a name
```
The code inside braces ({}) is parsed as a sequence of statements (i.e. `foo` is treated like a label, not a key in an object literal).

Remember to wrap the object literal in parentheses:

```JavaScript
var f = () => ({  foo: 1  });
```
##### [`<<`](../readme.md)