### Import only needed parts, not he whole module

```JavaScript
import {foo, bar} from "my-module";
```

### Import an entire module

```JavaScript
import * as myModule from "my-module";
```
> This inserts `myModule` into the current scope, containing all the exported bindings from "my-module.js".

### Import default

```JavaScript
import foo from "my-module";
```
> works only if imported module has default export

##### [`<<`](../README.md)