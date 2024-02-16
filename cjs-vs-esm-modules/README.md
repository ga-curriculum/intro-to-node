# ![Intro to Node - Level Up - CJS vs ESM Modules](./assets/hero.png)

**Learning Objective:** By the end of this lesson, students will understand the key differences between CommonJS (CJS) modules and ECMAScript modules (ESM) in JavaScript and when to use each type.

## CJS vs ESM

JavaScript modules come in two main flavors: CommonJS (CJS) and ECMAScript modules (ESM). Understanding their differences is important for writing code across environments and tooling ecosystems.

### CommonJS (CJS) modules

CommonJS (CJS) modules were created to address the lack of a native module system in JavaScript for server-side environments. Before ECMAScript Modules (ESM) were introduced, JavaScript did not have a built-in module standard, which made code organization and reuse more challenging in large-scale applications.

CommonJS modules filled this gap by providing a way to define encapsulated modules of code, which could then be used in other parts of a Node application.

#### Characteristics

- **Syntax**: Uses `require()` to import modules and `module.exports` to export.
- **Loading**: Synchronous loading makes it suitable for server-side applications where modules are all on the same machine.
- **Compatibility**: Native to Node and widely supported by most server-side frameworks.

#### Example

To require:

```javascript
const myModule = require('myModule');
```

To export:

```javascript
const myFunction = () => {
  console.log("Send me anywhere, I'm ready!");
};

module.exports = myFunction;
```

> 🧠 Explore [Node's CJS module documentation](https://nodejs.org/api/modules.html) for more on CommonJS.

### ECMAScript modules (ESM)

ECMAScript Modules are the modern, official standard for module management in JavaScript. They were created to provide a standard, built-in module system that could be used across different environments, including the browser and server-side (Node) contexts.

Before the introduction of ESM, JavaScript lacked a native module system, leading to the development of various non-standard module formats like CommonJS.

#### Characteristics

- **Syntax**: Uses `import` and `export` statements.
- **Loading**: Supports asynchronous loading, which is advantageous for client-side scripts where modules might be loaded over the network.
- **Compatibility**: Natively supported in modern browsers and Node.

#### Example

To import:

```javascript
import myModule from 'myModule';
```

To export:

```javascript
const myFunction = () => {
  console.log("Send me anywhere, I'm ready!");
};

export default myFunction;
```

> 🧠 Explore [Node's ESM documentation](https://nodejs.org/api/esm.html) for more on ECMAScript modules.

### When to use CommonJS modules

- **Node applications**: CommonJS is a great choice for building applications in Node because it's supported by default.
- **Working on existing projects or legacy code**: If you're working on a project that already uses CommonJS, it's usually best to stick with it for consistency.

### When to use ECMAScript modules

- **Web development**: ECMAScript modules are the only option for websites and web applications.
- **Starting new projects in Node**: If you're beginning a new project in Node and want to use the latest standards, ECMAScript modules are a good choice.
- **Sharing code between the browser and server**: If you plan to use the same code in both a web browser and a Node server, ECMAScript modules make this possible. ***CommonJS modules cannot be used for client-side code.***
