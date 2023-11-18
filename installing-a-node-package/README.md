# ![Intro to Node - Installing a Node Package](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will learn the basics of installing a node package.

## Using packages from npm

Now that you have a `package.json` file you can add a package from NPM to your project. We're going to add [validator](https://www.npmjs.com/package/validator) to our project - a wildly popular utility library. 

Use this command to add it:

```bash
npm i validator
```

> 🧠 The `i` in `npm i` is an alias for `install`!

> 📚 A *dependency* refers to an external library, module, or component that a project relies on to function correctly, providing pre-built functionality or reusable code to simplify development and reduce duplication of effort.

## Exploring `package.json`

Examining the `package.json` file reveals that it's structured something like this:

```JSON
{
  "name": "testvalidate",
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

Note that the property `dependencies` contains the property `validator`, which itself has the value `"^13.11.0"`.  This value is the version number for the installed package `validator`.  `npm` uses `package.json` as a reference to know all the following (and more) about a project's dependencies:

- The required version of the dependency.
- When or when not to install certain packages (dev-dependencies vs production dependencies).
- The circumstances in which a newer version of dependency should used.

The value of having this information in `package.json` is that it allows us to keep our dependencies out of our Git repos.  This saves space and bandwidth.  Once we clone the repo, we can than use `npm i` which will read the `package.json` file and install the missing dependencies easily.

To demonstrate this, first delete the `node_modules` directory.  This node project directory resembles how it might look immediately after you clone it in Git.  Remember that a Git repo is very similar to the project that was built, except it's missing the `node_modules` directory that contains the project's dependencies.

Now we can install all our app's dependencies as listed in `package.json` like this:

```bash
 npm i
```

If you look at the contents of the project's directory again, `node_modules` should have been recreated.  Using `npm i` allows us to install *all* the dependencies of a project, no matter how many there are, with just one command.  We could manually install each of those packages after cloning the repo, but that can be annoying and error prone once there are more than a few packages to install.