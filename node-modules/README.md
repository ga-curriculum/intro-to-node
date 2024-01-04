# ![Intro to Node - Node Modules](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to use import modules into their own code.

## Node modules

In the larger scope of programming, a module is a piece of code that can be reused in other pieces of code. In Node, a module is a JavaScript file that can be imported into other JavaScript files.

Let's view these modules through something we already know, like a house. In this house, we can have a couple of different modules to improve our living situation:

- Kitchen module - This module will allow us to cook food in our house.
- Bathroom module - This module will allow us to use the bathroom in our house.
- Bedroom module - This module will allow us to sleep in our house.
- Living room module - This module will allow us to relax in our house.

Like our house, we can have modules in our JavaScript code that allow us to do different things. For example, a module can enable us to do math, read and manipulate the file system, and even create a web server.

## Core modules

Node itself comes with several core modules, such as:

- [`http`](https://nodejs.org/api/http.html) - This module allows us to create a web server.
- [`fs`](https://nodejs.org/api/fs.html) - This module allows us to read and manipulate the file system.

> 📚 A list of core modules can be found [here](https://flaviocopes.com/node-core-modules/).

Before using any new technology, it's essential to read the documentation. Look at the documentation for the [`fs`](https://nodejs.org/api/fs.html) module. There are a lot of different methods that we can use to read and manipulate the file system. To create a file, we will use the [`writeFile`](https://nodejs.org/api/fs.html#fswritefilefile-data-options-callback) method.

According to the documentation, the `writeFile` method takes three parameters:

- `file` - A string containing the file's name to which it will be written.
- `data` - The text to write to the file.
- `callback` - A callback function that will execute once the method has finished creating the file.

> 📚 There is also an optional parameter called `options`. We can tell that this is an optional parameter in the documentation by the square brackets `[]` around the parameter name. This parameter is an object where we can declare some options when we execute our callback function, such as changing the encoding. You can read more about it [here](https://nodejs.org/api/fs.html#fs_fs_writefile_file_data_options_callback).

Let's apply these learnings to our code. Replace the code in `server.js` with the following:

```js
const fs = require('fs');

fs.writeFile('./hello.txt', 'hello, friend', () => {
  console.log('done creating file');
});
```

Braking down what is happening here:

- We are importing the `fs` module into our code.
- We are using the `writeFile` method to create a file called `hello.txt` with the text `hello, friend`.
- We use a callback function to log a message to the console once the file has been created.

The callback function is very similar to the callbacks we saw in Unit 1 when dealing with browser events, except the event here is the completion of creating the file (as opposed to a user-generated event like clicking). Node has many other events that take callbacks, and we'll see some of them while creating our web server applications.

## Review Questions

1. What is a module?
2. True or false: Node.js comes with several core modules.
3. True or false: When using a new technology, it's essential to read the documentation.