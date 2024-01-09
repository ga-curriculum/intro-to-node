# ![Intro to Node - Executing JavaScript with Node](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will understand the key differences between executing JavaScript in a web browser and in Node.js. 

## Executing JS with Node

Node's runtime environment for JavaScript is different than that in the browser, primarily because:

- It doesn’t have a browser’s DOM or [Web APIs](https://developer.mozilla.org/en-US/docs/Web/API).
- Node has low-level networking and file system APIs that the JavaScript browser does not (for security reasons).


To understand the distinct environments of a web browser and Node.js, let’s perform a simple experiment that highlights their differences.

### In the web browser

1. Open your web browser and access the console (usually found in Developer Tools).
2. Type and enter the following JavaScript command:

    ```js
    window;
    ```

> This command returns the `window` object, which represents the browser's window and includes methods and properties to manipulate the web page's content.

### In the terminal

The Node REPL (Read-Eval-Print Loop) is an interactive shell that lets you execute Node.js code line by line.

Open your terminal and start Node's REPL by typing:

```bash
node
```

Once in the Node REPL, type the following:

```js
window;
```

> You'll receive a `ReferenceError`, indicating that the `window` object is undefined in Node. This demonstrates that browser-specific objects like `window` and Web APIs are not available in Node.js.

We can further illustrate this point by trying to access a DOM element, which is a common browser operation:

```js
document.querySelector('body');
```

> Since the DOM is part of the web browser environment, this will also result in an error in Node.js.



### Testing Node features in the Browser

Just like how the `window` object is not defined in Node, some objects or modules that come with Node.js are not accessible in the browser. Back in your browser's console, type the following:

```js
fs;
```

You'll encounter a `ReferenceError` because the `fs` (File System) module is specific to Node.js and not defined in the browser.

Now, let's try this in your Node REPL. Type the following in the terminal:

```js
fs;
```

Unlike the browser, Node will return the `fs` module, which is used for file system operations in Node.js.

This experiment highlights how Node.js and browsers have distinct global objects and capabilities. Node excels with backend functionalities like file system access, while browsers are equipped for frontend tasks like DOM manipulation.

> 📚 For more information, refer to the Node.js documentation on the [*fs*](https://nodejs.org/api/fs.html) module.


## Running javascript files in the terminal

Now let's test how Node.js enables us to run JavaScript programs in the terminal. Copy the following JavaScript code into your `server.js` file:

```js
const multiply = (a, b) => {
    return a * b;
};

const product = multiply(5, 8);

console.log(product);
```

Back in the terminal, use the following to execute what we just wrote in `server.js`:

```bash
node server.js
```

> Tip: Press `ctrl` + `(backtick)` to open the integrated terminal in VS Code. You can run your code here just as you would your terminal application, and minimize the number of applications competing for screen space.