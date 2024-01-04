# ![Intro to Node - Installing a Node Package](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will learn the basics of installing a node package.

## Using packages from NPM

Now that you have a `package.json` file, you can add a package from NPM to your project. We will add [validator](https://www.npmjs.com/package/validator) to our project.

ValidatorJS is a package that provides lots of practical methods for validating and sanitizing strings, such as:

- `isDate()` - Validates that the string is a date.
- `isEmail()` - Validates that the string is an email.
- `toBoolean()` - Converts the string to a boolean.
- `normalizeEmail()` - Normalizes the string to an email.

We are going to install this package using NPM:

```bash
npm i validator
```

> 🧠 The `i` in `npm i` is an alias for `install`!

## Exploring `package.json`

Examining the `package.json` file reveals that it's structured something like this:

```JSON
{
  "name": "intro-to-node",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
    "validator": "^13.11.0"
  }
}
```

Note that the property `dependencies` contains the property `validator`, which has the value `"^13.11.0"`. This value is the version number for the installed package `validator`. NPM uses `package.json` as a reference to know all the following (and more) about a project's dependencies:

- The required version of the dependency.
- When or not to install specific packages (dev-dependencies vs production dependencies).
- The circumstances in which a newer version of dependency should used.

This information is valuable in `package.json` because it allows us to keep our dependencies out of our Git repos. This saves space and bandwidth. Once we clone the repo, we can use `npm i`, which will read the `package.json` file and easily install the missing dependencies.

To demonstrate this, first delete the `node_modules` directory. This node project directory resembles how it might look immediately after you clone it from a Git repo. Remember that a Git repo is very similar to the project built, except it's missing the `node_modules` directory containing the project's dependencies.

Now we can install all our app's dependencies as listed in `package.json` like this:

```bash
npm i
```

If you look at the contents of the project's directory again, `node_modules` should have been recreated. Using `npm i` allows us to install *all* the project dependencies, no matter how many there are, with just one command. We could manually install each of those packages after cloning the repo, but that can be annoying and error-prone once more than a few packages are installed.