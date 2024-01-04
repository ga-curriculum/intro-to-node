# ![Intro to Node - Node Modules](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to use import modules into their own code.
## Node modules

In a Node application, **every** JavaScript file is a *module*! Modules in Node allow us to **modularize** and **reuse** code in a Node app.

> 📚 A JavaScript module is a self-contained piece of code that encapsulates related functionality and can be imported and used in other JavaScript files, promoting modular programming, code organization, and reusability.

## Core modules

Node itself comes with several core modules, such as the `http` and `fs` modules. A list of core modules can be found [here](https://flaviocopes.com/node-core-modules/).

Let's use the core `fs` module to create a file. Replace the code in `server.js` with this:

```js
const fs = require('fs')

fs.writeFile('./hello.txt', 'hello, friend', () => {
  console.log('done creating file')
})
```

Each module that we `require` defines what is returned by the invocation of `require()`.  For instance, the `fs` module used above tells Node what will be returned when we call `require('fs')`.  To figure out what will be returned, we'll need to read the documentation for that module.  A different module like `http` will have `require` return something else, so whenever requiring a module, it's important to read the documentation that corresponds to it, so we know how to use it.

After reading [the documentation for fs](https://nodejs.org/api/fs.html) we can figure out that `require('fs')` will return an object with several methods on it, each dedicated to manipulating files on your computer.  Note, that you don't have to read all of the documentation for `fs`.  Scan through it and see what sense you can make of it.  With practice, you'll get better and quicker at looking through documentation to find the information you're looking for.  Now that we know that `require('fs')` returns an object with methods on it, we assign that result to the variable `fs`, so that we can use it later in our code.

Notice `fs`'s `writeFile` method that we invoke on the next line to create a file.  According to the documentation it takes three parameters:

- a string containing the name of the file to which it will write
- the text to write to the file
- a callback function that will execute once the method has finished creating the file

The callback function is very similar to the callbacks we saw in Unit 1 when we were dealing with browser events, except the event here is the completion of creating the file (as opposed to a user generated event like clicking).  Node has lots of other events that take callbacks, and we'll see some of them while creating our web server applications.