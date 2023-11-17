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

console.log(typeof fs)
console.log(fs)

fs.writeFile('./hello.txt', 'hello, friend', () => {
  console.log('done creating file')
})
```

We can see that the `fs` module exports an object that has methods such as `writeFile`.  

Notice that `writeFile` takes as a third parameter, a callback function that executes once it's finished creating the file.  This is very similar to the callbacks we saw in Unit 1 when we were dealing with browser events, except the event here is the completion of creating the file.  Node has lots of other events that take callbacks, like the one above, and we'll see some of them while creating our web server applications.