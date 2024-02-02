# ![Intro to Node - Level Up - CJS vs ESM Modules](./assets/cjs-vs-esm-modules.png)

**Learning Objective:** Understand the key differences between CommonJS (CJS) modules and ECMAScript Modules (ESM) in JavaScript and when to use each type.

## CJS vs ESM

JavaScript modules come in two main flavors: CommonJS (CJS) and ECMAScript Modules (ESM). Understanding their differences is important for communicating between files in Javascript.

### CommonJS (CJS) modules

CommonJS (CJS) modules were created to address the lack of a native module system in JavaScript for server-side environments, particularly in Node.js. Before ECMAScript Modules (ESM) were introduced, JavaScript did not have a built-in module standard, which made code organization and reuse more challenging in large-scale applications. CommonJS modules filled this gap by providing a simple and straightforward way to define encapsulated modules of code, which could then be easily imported and used in other parts of a Node.js application. 

#### Characteristics:

- **Syntax**: Uses `require()` to import modules and `module.exports` to export.
- **Loading**: Synchronous loading, making it suitable for server-side applications where modules are located on the same machine.
- **Compatibility**: Native to Node.js and widely supported in many server-side frameworks.

#### Example:

To import:

```javascript
const myModule = require('myModule');
```

To export:

```javascript
const myFunction = () => {
  console.log("Send me anywhere, Im ready!")
}

module.exports = myFunction;
```

> Explore the [Node module documentation](https://nodejs.org/api/modules.html) for more on CommonJS.

### ECMAScript modules (ESM)

ECMAScript Modules are the modern, official standard for module management in JavaScript. They were created to provide a standard, built-in module system that could be used across different environments, including both browser and server-side (Node) contexts. Prior to the introduction of ESM, JavaScript lacked a native module system, leading to the development of various non-standard module formats like CommonJS.

#### Characteristics:

- **Syntax**: Uses `import` and `export` statements.
- **Loading**: Supports asynchronous loading, which is advantageous for client-side scripts where modules might be loaded over the network.
- **Compatibility**: Natively supported in modern browsers and increasingly in Node.js (from version 13.2.0, with `.mjs` file extension).

#### Example:


To import:

```javascript
import myModule from 'myModule';
```

To export: 

```javascript
const myFunction = () => {
  console.log("Send me anywhere, Im ready!")
}

export default myFunction;
```

> Node.js added [official support for ES modules](https://nodejs.org/api/esm.html#esm_modules_ecmascript_modules) in version 12.

> 💡 Why `.mjs`?: Node treats `.js` files as CommonJS modules by default. To explicitly indicate that a file is an ES module, we use the `.mjs` file extension.


### When to use CommonJS modules:

 - **Node.js Applications**: CommonJS is a great choice for building applications in Node.js. It's simple to use and works well because Node.js supports it by default.
 - **Working on Existing Projects or Legacy code**: If you're working on a project that already uses CommonJS, it's usually best to stick with it for consistency.

### When to use ECMAScript modules:

- **Web Development**: ECMAScript modules are ideal for websites and web applications. They work well in modern web browsers and help organize your JavaScript code efficiently. *CommonJs modules cannot be used for client side code.*
- **Starting New Projects in Node.js**: If you're beginning a new project in Node.js and want to use the latest standards, ECMAScript modules are a good choice.
- **Sharing Code Between Browser and Server**: If you plan to use the same code in both a web browser and a Node.js server, ECMAScript modules can make this easier.