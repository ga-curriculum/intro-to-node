# ![Intro to Node - Level Up - What is `.mjs`?](./assets/hero.png)

Before ES6, when *ESM (ECMAScript Modules)* was introduced, modules were not implemented officially in the JavaScript specification, so Node relied on the CommonJS module system. Node added [official support for ES modules](https://nodejs.org/api/esm.html#esm_modules_ecmascript_modules) in Node 12. Still, to preserve legacy code behavior, Node treats files with the `.js` extension as CommonJS modules.

> 📚 *ESM* is the official module system introduced in ES6 to provide a standardized way to organize and share JavaScript code across client-side and server-side environments.

*CommonJS* uses a different syntax to import (`require()`) and export (`module.exports`) code between modules. We will not cover these as part of the course material - but you should familiarize yourself with how they function because you'll likely see them in the wild. Check out the [Node module documentation](https://nodejs.org/api/modules.html) for more.

> 📚 *CommonJS* is a module format and specification that defines a standard for organizing and sharing JavaScript code in server-side environments, primarily used in Node.js.

While CommonJS was initially designed for server-side JavaScript and became the de facto module standard for Node.js, ESM is the modern and native module system compatible with browsers and Node.js. The ESM syntax is more concise, offers better support for static analysis and tree shaking (eliminating unused code), and facilitates better performance through asynchronous loading. For these reasons, along with it being supported in all current Node versions, we will be using ES modules in this course.

We us the `.mjs` file extension to indicate that a file is an ES module. This is because Node treats files with the `.js` extension as CommonJS modules.
