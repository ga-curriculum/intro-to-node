# ![Intro to Node - Importing Node Packages in a Script](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will learn the basics of importing node packages in a script.

## Importing CommonJS Modules into Your App

Now that we've installed the ValidatorJS package, let's use one of its methods in our app. Taking a look a the NPM page for this package [here](https://www.npmjs.com/package/validator#no-es6) we can see an example of how to require and us the `isEmail` method. Let's do that in our `server.js` file:

```js
const validator = require('validator');
console.log(validator.isEmail('foo@bar.com'));
```

> 🧠 Notice that we changed over the `var` keyword to `const`. Whenever possible we should use `const` or `let` instead of `var`. When requiring it's always best to use `const` becauce we don't want the value of our `validator` to be reassigned. Also see that we have wrapped `validator.isEmail('foo@bar.com')` in a `console.log()` statement. This will allow us to see the result of the `isEmail()` method in the terminal.

`require('validator')` imports the Validator package into the `server.js` file. The Validator NPM package itself defines what the `require()` invocation will return when importing that particular package. This is just like the previous example with `fs`. Each NPM package will have `require()` return something different, so it's important to consult each package's documentation to determine what the result of `require()` will be.

We take the result of `require('validator')` (that object with the methods on it) and assign it to a the variable `validator` so that we can use it in our code. In the example above, we invoke the `isEmail` method to validate that `'foo@bar.com'` is a properly formatted email address. As it turns out, `isEmail` will return `true` if it's valid and `false` otherwise. There's no way to know this (or really anything about any NPM package) without consulting the package's documentation, so using any NPM package involves a decent amount of documentation scanning. Being comfortable doing this takes practice, but it's a critical skill to develop.

Most NPM packages will have their NPM registry page, the one we have viewed and then a sepretate GitHub page. The GitHub page will have more detailed documentation on how to use the package. For example, the Validator NPM registry page is [here](https://www.npmjs.com/package/validator) and the GitHub page is [here](https://github.com/validatorjs/validator.js). 

> 🧠 Some large packages even have their own webisite with documentation. In most cases these packages will have a link to their website on their NPM registry page along with any GitHub documentation they may have.

Run node `server.js` to try it out.

```bash
$ node server.js
```

You should see `true` printed to the terminal.

## 🎓 You do

Using the GitHub page [here](https://github.com/validatorjs/validator.js) as a reference, use the `isDate()` method to validate that `'2020-12-31'` is a date. Print the result to the terminal.