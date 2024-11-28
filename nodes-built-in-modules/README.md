<h1>
  <span class="headline">Intro to Node</span>
  <span class="subhead">Node's Built-in Modules</span>
</h1>

**Learning objective:** By the end of this lesson, students will understand the concept of modules by learning how to require and use core Node modules, such as `fs`, in their applications.

## Node's built-in modules

In the broad context of programming, a *module* is a reusable block of code. In Node specifically, a module refers to a JavaScript file that can be easily used in other JavaScript files, allowing for code reuse and modular programming.

Think of modules as the rooms in a house, where each room serves a specific purpose. In a home, the kitchen is used for cooking meals. A living room offers space for relaxation and entertainment. A garage provides a place to store a vehicle.

Each module in Node, like a room in a house, is designed for a particular set of tasks, making the overall structure of an application functional and organized. Like you wouldn't cook a meal in your bathroom, you won't use the same module to handle user events and connect to a database.

> 📚 A *module* is a self-contained unit of code that encapsulates a specific functionality, which can be easily used in other parts of a program.

## Core modules in Node

Node has a set of built-in core modules, each designed for specific functionalities. Among these are:

- **[`http`](https://nodejs.org/api/http.html)**: Enables the creation and handling of a web server.
- **[`fs`](https://nodejs.org/api/fs.html)**: Provides the capability to read from and write to the file system.

A comprehensive list of Node core modules is available [here](https://flaviocopes.com/node-core-modules/).

### The importance of documentation

Before using any module, familiarizing yourself with its documentation is crucial. For example, the [`fs`](https://nodejs.org/api/fs.html) module's documentation details various methods to interact with the file system.

#### Understanding `writeFile()`

One of the methods, [`writeFile()`](https://nodejs.org/api/fs.html#fswritefilefile-data-options-callback), is used for creating files. It requires three parameters:

- `file`: A string specifying the file's name.
- `data`: The content to be written to the file.
- `callback`: A function that executes after the file is created.

Additionally, there's an `options` parameter, which is optional. This is communicated in the documentation by being enclosed in square brackets as shown here: `fs.writeFile(file, data[, options], callback)`. Using square brackets to indicate optional parameters is a common pattern in JavaScript documentation.

### Implementing `writeFile()`

Let's put this into practice. In your `server.js` file, write:

```javascript
const fs = require('fs');

fs.writeFile('./hello.txt', 'hello, friend', () => {
  console.log('done creating file');
});
```

#### What's happening in the code

- **Requiring the `fs` module**: The `fs` module is required, making its functionality accessible.
- **Using `writeFile()`**: We utilize `writeFile()` to create a `hello.txt` file and write the text `hello, friend` into it.
- **Callback function**: A callback function logs a message to the console upon file creation.

This callback function in Node is conceptually similar to callbacks in browser event handling. However, here, it responds to a new type of event - the end of the file creation process.
