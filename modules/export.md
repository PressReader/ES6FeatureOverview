### Export functions, objects or primitives

```JavaScript
export function cube(x) {
  return x * x * x;
}

const foo = Math.PI + Math.SQRT2;
export { foo };
```
> multiple per script

### Default exports
```JavaScript
export default function (x) {
  return x * x * x;
}
// or export default class {}
```
>  only one per script
##### [`-> import`](import.md)