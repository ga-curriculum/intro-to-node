# ![Intro to Node - Installing a Node Package](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will learn the basics of installing and using an NPM package from the NPM package registry.

## Installing packages in a project

With your `package.json` file in place, you're now ready to enhance your project by adding packages from the NPM registry.

### Installing a package

Let's choose a practical package called `ValidatorJS` for our example. It offers a variety of string validation and sanitization methods, such as:

 - `isDate()`
 - `isEmail()`
 - `toBoolean()`
 - `normalizeEmail()`
 
 These kinds of methods might be useful to us if were were collecting information from a user and needed to verify that it was ina specific format.  While we could write this code ourselves, using a package someone else has already written saves time!

To install this package, use the following NPM command:

```bash
npm i validator
```

> 🧠 *Note*: The `i` in `npm i` is a shorthand for `install`.

### The installation process

- **Package Download**: When you run `npm i validator`, NPM downloads the `ValidatorJS` package code from the npmjs.com registry to your local machine.

- **Where does this code live?**: The downloaded package code is stored in the `node_modules` directory that just appeared in your project folder. This is where all your installed packages are stored.

- **Using the Package**: To use `ValidatorJS` in your code, you need to import it into your JavaScript files, typically with a `require` statement.

### Exploring `package.json` post-installation

After installing a package, the `package.json` is updated to reflect this change:

```json
{
  "name": "intro-to-node",
  "version": "1.0.0",
  ...
  "dependencies": {
    "validator": "^13.11.0"
  }
}
```

- **Dependencies**: The `dependencies` property now includes `validator`, with `^13.11.0` indicating the installed version.

- **Version Management**: The version number helps NPM manage compatibility and updates. The caret `^` symbol allows minor updates that don't break compatibility.


## Can I delete or uninstall packages? 

Yes, npm makes it easy to manage your packages and delete or reinstall when necessary. 

To **remove a package** from your project, use:

```bash
npm uninstall <package-name>
```

This command not only deletes the package from the `node_modules` folder but also removes it from your `package.json` file, ensuring that your project and its dependency list remain synchronized.

## Reinstalling node modules

There might be situations where you need to delete and reinstall all your project's dependencies. NPM makes it easy by keeping inventory of your packages in the `package.json` file. 

Reinstalling is as easy as running `npm install`.

Let's try it! 

## 🎓 You Do

1. First, delete the `node modules` directory. **Don't worry.** You can safely delete this entire directory without losing your project's dependency information.

2. **Reinstall** it by running the command:

    ```bash
    npm i
    ```

    Observe how NPM automatically recreates the `node_modules` folder with all the necessary packages based on the `package.json`.

## Keeping `node_modules` out of git repositories

As you install more dependencies, the `node_modules` directory can become large. Keeping it out of Git repositories saves space and makes cloning the repository faster.

- The `package.json` file in your Node.js project acts like an inventory list. It meticulously tracks all the packages your project depends on, including their specific versions.

- Because `package.json` contains all this essential information, there's no need to upload the actual Node modules to your Git repository. Instead, any developer can set up the project environment by simply running `npm install`. This command reads the `package.json` file and automatically downloads all the required Node modules.

- When you clone a repository, the `node_modules` directory isn't included. Running `npm install` will recreate it by installing all packages listed in `package.json`.

> 📚 To prevent Git from tracking your `node_modules`, add it to a `.gitignore` file. This file tells Git which directories and files to ignore.