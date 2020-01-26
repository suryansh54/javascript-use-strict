# Use Strict

- "use strict"; Defines that JavaScript code should be executed in "strict mode".
- The "use strict" directive was new in ECMAScript version 5.
- It is not a statement, but a literal expression, ignored by earlier versions of JavaScript.
- The purpose of "use strict" is to indicate that the code should be executed in "strict mode".
- With strict mode, you can not, for example, use undeclared variables.
- All modern browsers support "use strict" except Internet Explorer 9 and lower:

```javascript
"use strict";
x = 3.14;       // This will cause an error because x is not declared
```

```javascript
"use strict";
myFunction();

function myFunction() {
  y = 3.14;   // This will also cause an error because y is not declared
}
```

```javascript
x = 3.14;       // This will not cause an error.
myFunction();

function myFunction() {
  "use strict";
  y = 3.14;   // This will cause an error
}
```

```javascript
function sum(a, a, c) { // !!! syntax error
  'use strict';
  return a + a + c; // wrong if this code ran
}
// Duplicate parameter name not allowed in this context
```
