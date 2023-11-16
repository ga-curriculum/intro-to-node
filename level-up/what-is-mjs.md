# ![Intro to Node - Level Up - What is `.mjs`?](./assets/hero.png)

Before ES6, when *ESM (ECMAScript Modules)* were introduced, modules were not implemented officially in the JavaScript specification, so Node relied on the CommonJS module system. Node added [official support for ES modules](https://nodejs.org/api/esm.html#esm_modules_ecmascript_modules) in Node 12, but to preserve legacy code behavior, node treats files with the `.js` extension as CommonJS modules.

> 📚 *ESM* is the official module system introduced in ES6 to provide a standardized way to organize and share JavaScript code across client-side and server-side environments.

*CommonJS* uses a different syntax to import (`require()`) and export (`module.exports`) code between modules. We will not cover these as part of the course material - but you should familiarize yourself in how they function, because you'll likely see them in the wild. Check out the [node module documentation](https://nodejs.org/api/modules.html) for more.

> 📚 *CommonJS* is a module format and specification that defines a standard for organizing and sharing JavaScript code in server-side environments, primarily used in Node.js.

While CommonJS was initially designed for server-side JavaScript and became the de facto module standard for Node.js, ESM is the modern and native module system that is compatible with both browsers and Node.js. The ESM syntax is more concise, offers better support for static analysis and tree shaking (elimination of unused code), and facilitates better performance through asynchronous loading.  For these reasons, along with it being supported in all current versions of Node, we're going to be using ES modules in this course. 

For now, we're going to need to inform node directly that we want to treat our files as ES modules - this is what the `.mjs` file extension accomplishes for us. We'll eventually have another method to tell Node that our files are ES modules, but that's for a later time..

**tl;dr**: for now add the `.mjs` file extension to your files. This file extension tells Node that the file is an ES module. We'll eventually show you a method that won't require you to do this and you can get back to using the `.js` extension for all your files.