# ![Intro to Node - Executing JavaScript with Node](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to use node to execute JavaScript.

## Executing JS with node

Now that you’ve learned how awesome Node is, let’s see how it runs JavaScript programs.

Type the following JavaScript in `server.mjs`:
```js
const multiply = (a, b) => a * b

let n = multiply(5, 8)
 	
console.log(n)
```

Press `ctrl` + `(backtick)` to open the integrated terminal in VS Code and type the following to execute what we just wrote in `server.mjs`:

```bash
node server.mjs
```

Yep, running a Node app is that easy! 


## Node modules

In a Node application, **every** JavaScript file is a *module*! Modules in Node allow us to **modularize** and **reuse** code in a Node app.

> 📚 A JavaScript module is a self-contained piece of code that encapsulates related functionality and can be imported and used in other JavaScript files, promoting modular programming, code organization, and reusability.

## Core modules

Node itself comes with several core modules, such as the `http` and `fs` modules. A list of core modules can be found [here](https://flaviocopes.com/node-core-modules/).

There are also thousands of open-source modules available.


Let's use the core `fs` module to create a file. Replace the code in `server.mjs` with this:

```js
import * as fs from 'fs'

console.log(typeof fs)
console.log(fs)

fs.writeFile('./hello.txt', 'hello, friend', function() {
  console.log('done creating file')
})
```

We can see that the `fs` module exports an object that has methods such as `writeFile`.

## Node modules of our own
Okay, now let’s see how we can create more modules of our own.

A Node app’s modules (files) can be put in any folder within the project. This allows us to create modules inside aptly named folders, such as `**models**`, `**routes**`, `**controllers**`, `**views**`, etc.


## Building more modules

Let’s create a file/module named `days-of-week.mjs`: 

```bash
touch days-of-the-week.mjs
```

Add some code to the new file:
```js
const daysOfTheWeek = [
  'Sunday',
  'Monday',
  'Tuesday',
  'Wednesday',
  'Thursday',
  'Friday',
  'Saturday'
]

console.log(daysOfTheWeek)
```

Even the file we run using `node` is a module, so let’s type `node days-of-the-week.mjs` and check out what’s logged.

**This is a key point to remember:** We can export *anything* from a module, we also have the power to choose what is exported and what is not. Whatever we include in the export statement can be imported in another module!

Let's verify this by adding to the **`days-of-the-week.mjs`** module.

```js
const myFavoriteDay = 'Saturday'

const saturday = {
  weekday: false,
  good: true,
  quote: 'Saturdays do indeed exist.'
}

function randomDay() {
  return daysOfTheWeek[Math.floor(Math.random() * daysOfTheWeek.length)]
}
```

And then exporting everything we've built so far from it at the bottom of the file:

```js
export {
  daysOfTheWeek,
  myFavoriteDay,
  saturday,
  randomDay,
}
```

Now let's import the module inside of `server.mjs` by replacing the code we've written there with this:

```js
import * as daysOfTheWeek from './days-of-the-week.mjs'

console.log(daysOfTheWeek)
```

You'll see everything we are exporting from the `**./days-of-the-week.mjs**` module being logged

Each module is uniquely identified by its fully qualified filename. This identifier allows modules to be named the same, as long as they exist in different folders.

Note that when we require our app's custom modules, we need to provide a relative path - always starting with either a `.` or `..`. By convention, we name the variable the same as, or as similar as possible to, the name of the module we have required.

> 🧠 You Do
> - Export something new from `./days-of-the-week.mjs`.
> - Run `server.mjs` to check it out.


> ❓ Review Questions
> 1. What are modules used for in Node?
> 2. How many times can we `import` a module in our program?


