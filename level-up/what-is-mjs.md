# ![Intro to Node - Level Up - What is .mjs?](./assets/hero.png)

## Understanding .mjs in Node.js

Node.js has evolved over the years in how it handles JavaScript modules. Let's dive into the specifics of `.mjs` and its role in Node.js.

### The shift from CommonJS to ESM

- **Before ES6 and ESM**: Prior to the introduction of *ESM (ECMAScript Modules)* in ES6, JavaScript did not have an official module system. Node.js relied on the *CommonJS* module system for organizing and sharing code.
- **Node's Support for ESM**: Node.js added [official support for ES modules](https://nodejs.org/api/esm.html#esm_modules_ecmascript_modules) in version 12. However, it continues to treat `.js` files as CommonJS modules to maintain compatibility with existing code.

> 📚 *ESM* (ECMAScript Modules): This is the official module system introduced in ES6, providing a standardized way to organize and share JavaScript code in both client-side and server-side environments.

### Understanding CommonJS

- **CommonJS Syntax**: CommonJS uses `require()` for importing and `module.exports` for exporting code between modules. While not covered extensively in this course, familiarity with CommonJS is important due to its prevalence in existing code.
- **Further Reading**: Explore the [Node module documentation](https://nodejs.org/api/modules.html) for more on CommonJS.

> 📚 *CommonJS*: A module format and specification for server-side JavaScript, primarily used in Node.js.

### Embracing ESM in modern development

- **Benefits of ESM**: ESM is more concise, supports better static analysis and tree shaking (removing unused code), and enables asynchronous loading. It's compatible with both browsers and Node.js.
- **Course Focus on ESM**: Due to its modern features and support in current Node versions, this course will focus on using ES modules.

### The role of `.mjs`

- **Why `.mjs`?**: Node treats `.js` files as CommonJS modules by default. To explicitly indicate that a file is an ES module, we use the `.mjs` file extension.

By understanding the difference between `.mjs` and `.js` in Node.js, you'll be better equipped to work with different module systems and their respective syntaxes.
