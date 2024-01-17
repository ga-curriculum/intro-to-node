# ![Intro to Node - Level Up - CJS vs ESM Modules](./assets/hero.png)

**Learning Objective:** Understand the key differences between CommonJS (CJS) modules and ECMAScript Modules (ESM) in JavaScript and when to use each type.

## CJS vs ESM

JavaScript modules come in two main flavors: CommonJS (CJS) and ECMAScript Modules (ESM). Understanding their differences is important for communicating between files in Javascript.

### CommonJS (CJS) modules

CommonJS modules are widely used in Node.js environments. They are known for their simplicity and ease of use, especially for server-side development.

#### Characteristics:

- **Syntax**: Uses `require()` to import modules and `module.exports` to export.
- **Loading**: Synchronous loading, making it suitable for server-side applications where modules are located on the same machine.
- **Compatibility**: Native to Node.js and widely supported in many server-side frameworks.

#### Example:

```javascript
const myModule = require('myModule');
module.exports = myFunction;
```

> Explore the [Node module documentation](https://nodejs.org/api/modules.html) for more on CommonJS

### ECMAScript modules (ESM)

ECMAScript Modules are the official standard for module management in JavaScript. They are designed to be more efficient and provide better static analysis.

#### Characteristics:

- **Syntax**: Uses `import` and `export` statements.
- **Loading**: Supports asynchronous loading, which is advantageous for client-side scripts where modules might be loaded over the network.
- **Compatibility**: Natively supported in modern browsers and increasingly in Node.js (from version 13.2.0, with `.mjs` file extension).

#### Example:

```javascript
import myModule from 'myModule';
export default myFunction;
```

> Node.js added [official support for ES modules](https://nodejs.org/api/esm.html#esm_modules_ecmascript_modules) in version 12.

> 💡 Why `.mjs`?: Node treats `.js` files as CommonJS modules by default. To explicitly indicate that a file is an ES module, we use the `.mjs` file extension.


### When to use CommonJS modules:

- **Server-side Development**: For Node.js server-side applications, CJS is often the go-to choice due to its synchronous nature and native support.
- **Legacy Projects**: For existing projects built on Node.js that haven't migrated to ESM.

### When to use ECMAScript modules:

- **Front-end Development**: Use ESM for client-side JavaScript due to its support for asynchronous loading and modern browser compatibility.
- **New Node.js Projects**: For new server-side projects in Node.js, consider using ESM, especially as Node.js moves towards ESM as the standard.
- **Cross-Environment Compatibility**: If you aim for a module to be compatible with both browser and server environments.

