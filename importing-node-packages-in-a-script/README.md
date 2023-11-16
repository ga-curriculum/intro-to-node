# ![Intro to Node - Importing Node Packages in a Script](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will learn the basics of importing node packages in a script.

## Importing CommonJS Modules into ES Modules

You'll frequently need to import CommonJS Modules from npm into ES Modules. For example, when you see [documentation](https://www.npmjs.com/package/validator) that directs you to use `require()` like this:

```js
const validator = require('validator')
```

You can accomplish the import into an ES module with this syntax:

```js
import alias from 'nameOfModule'
```

This is syntactic sugar for this syntax:

```js
import { default as alias } from 'nameOfModule'
```

Demonstrating using our validator example above:

```js
import validator from 'validator'
```

We can now import the validator package in `server.mjs` and use it!

```js
import validator from 'validator'

console.log(validator.isEmail('foo@bar.com'))
```

Run node `server.mjs` to try it out.

## Exploring `package.json`

Examining the `package.json` file reveals that it's structured something like this:

```JSON
{
  "name": "first-node",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC"
}
```

`npm` uses `package.json` as a reference to know all the following (and more) about a projects dependencies:
- The required version of the dependency.
- When or when not to install certain packages (dev-dependencies vs production dependencies).
- The circumstances in which a newer version of dependency should used.
`node` also uses it to determine things like the main script, and what module system is used by a project. Let's tell it we're going to use ES modules by adding this line right before the `"license"` line.


```bash
"type": "module",
```

Now node knows our project uses ES modules, so we don't have to use the `**.mjs**` extension on our files anymore! You can rename `**server.mjs**` to `**server.js**` and `**days-of-the-week.mjs**` to `**days-of-the-week.js**`, and the project should still function error free.

Installing dependencies is necessary after cloning a repo or when using the starter code for a lesson. To demonstrate this, first delete the `node_modules` file.

Now we can install all our app's dependencies as listed in `**package.json**` like this:

```bash
 npm i
```

> 📚 The `package.json` file is a located in the root directory of a Node.js project. It contains metadata, dependencies, scripts, and configuration information for the project. The details in this file help to standardize and manage JavaScript projects, making it easier to share, collaborate, and maintain consistency across different execution environments.