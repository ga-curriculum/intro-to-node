# ![Intro to Node - Node's Built in Modules](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will understand the concept of modules by learning how to import and use both custom and core Node.js modules, such as `fs`, in their applications.

## Node's built in modules

In the broad context of programming, a *module* is essentially a reusable block of code. In Node.js specifically, a module refers to a JavaScript file which can be easily imported and used in other JavaScript files, allowing for code reuse and modular programming.

In Node.js, think of modules as different rooms in a house, where each room serves a specific purpose:

- **Kitchen Module**: Like a kitchen used for cooking, a module in Node.js might handle specific tasks like calculations or data processing.
- **Living Room Module**: Similar to a living room used for relaxation and entertainment, another module could manage interactions with users or handle user inputs.
- **Bedroom Module**: Just as a bedroom provides a place to rest, a module in Node.js might be dedicated to maintaining and managing the state of the application, like a user's session data.

Each module in Node.js, like a room in a house, is designed for a particular set of tasks, making the overall structure (the application) functional and organized.


> 📚 A *module* is a self-contained unit of code that encapsulates a specific functionality, which can be easily imported and used in other parts of a program.

## Core modules in Node.js

Node.js is equipped with a set of built-in core modules, each designed for specific functionalities. Among these are:

- **[`http`](https://nodejs.org/api/http.html)**: Enables the creation and handling of a web server.
- **[`fs`](https://nodejs.org/api/fs.html)**: Provides the capability to read from and write to the file system.

A comprehensive list of Node.js core modules is available [here](https://flaviocopes.com/node-core-modules/).

### The importance of documentation

Before using any module, familiarizing yourself with its documentation is crucial. For example, the [`fs`](https://nodejs.org/api/fs.html) module's documentation details various methods to interact with the file system. 

#### Understanding `writeFile`

One of the methods, [`writeFile`](https://nodejs.org/api/fs.html#fswritefilefile-data-options-callback), is used for creating files. It requires three parameters:
- `file`: A string specifying the file's name.
- `data`: The content to be written to the file.
- `callback`: A function that executes once the file is created.

Additionally, there's an optional `options` parameter. Enclosed in square brackets in the documentation, this object allows you to specify options like encoding. More on this [here](https://nodejs.org/api/fs.html#fs_fs_writefile_file_data_options_callback).

### Implementing `writeFile`

Let's put this into practice. In your `server.js` file, write:

```javascript
const fs = require('fs');

fs.writeFile('./hello.txt', 'hello, friend', () => {
  console.log('done creating file');
});

```

#### What's Happening in the Code:

- **Importing the `fs` Module**: The `fs` module is imported, making its functionality accessible.
- **Using `writeFile`**: We utilize `writeFile` to create a `hello.txt` file, writing `hello, friend` into it.
- **Callback Function**: A callback function logs a message to the console upon file creation.

This callback function in Node.js is conceptually similar to callbacks in browser event handling. However, here it responds to the completion of a file creation process. As we explore Node.js further, especially in web server application development, we'll encounter various such Node.js-specific events and their associated callbacks.
