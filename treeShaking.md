# Tree Shaking

**Tree shaking** is a term commonly used in JavaScript to describe the **removal of dead code**.

It relies on **import** and **export** statements in ES6 to determine which modules are imported and exported between files.

Tree shaking starts from entry points and only includes the code that can ever be executed.

To remove dead code, we need to use tools such as **Webpack** and **UglifyJS**.

Example:

src/utils.js

```javascript
export function add(a,b){
    return a + b;
}

export function multiply(a, b){
    return a * b;
}
```

src/index.js

```javascript
import { add } from utils.js;

function main(){
    add(1, 2);
}
```

In the `main.js` file, we only imported `add` from the file `utils.js`, so the function `multiply` is dead code.

If we have a basic Webpack setup to bundle our files, after running `npm run build`, we can see the output bundle look something like this:

```javascript
/* 1 */
/***/ (function(module, __webpack_exports__, __webpack_require__) {

"use strict";
/* unused harmony export multiply */
/* harmony export (immutable) */ __webpack_exports__["a"] = add;
function add(x, x){
    return x + x;
}

function multiply(x, x){
    return x * x;
}
```

If you look above, you can see that the function `multiply` is not being exported, however, it is still present in the bundle.

This can be fixed by using tools like **UglifyJS** that will minify the code and remove the dead code from the final bundled file.

**Webpack by itself does not perform tree shaking, it needs tools like UglifyJS to perform actual dead code elimination.**

