# ![Intro to Node - Importing Node Packages in a Script](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will learn the basics of importing node packages in a script.

## Importing CommonJS Modules into Your App

Now that we've installed the Validator package, let's use it.  In your `server.js` file, add the following:

```js
const validator = require('validator');
console.log(validator.isEmail('foo@bar.com'))
```

Run node `server.js` to try it out.

`require('validator')` imports the Validator package into the `server.js` file.  The Validator NPM package itself defines what the `require()` invocation will return when importing that particular package.  This is just like the previous example with `fs`.  Each NPM package will have `require()` return something different, so it's important to consult each package's documentation to determine what the result of `require()` will be.  By viewing the [Validator documentation](https://github.com/validatorjs/validator.js),  we're able to determine that `require('validator')` will return an object that has many methods on it, each used to validate strings.

We take the result of `require('validator')` (that object with the methods on it) and assign it to a the variable `validator` so that we can use it in our code.  In the example above, we invoke the `isEmail` method to validate that `'foo@bar.com'` is a properly formatted email address.  `isEmail` will return `true` if it's valid and `false` otherwise.  There's no way to know this (or really anything about any NPM package) without consulting the package's documentation, so using any NPM package involves a decent amount of documentation reading.  Being comfortable doing this takes practice, but it's a critical skill to develop.