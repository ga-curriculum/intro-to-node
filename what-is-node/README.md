# ![Intro to Node - What is Node.js?](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be introduced to Node.js and its significance.

## What is Node.js?

JavaScript can be interpreted by a couple of different environments. The most common environment is the browser. However, JavaScript can also be interpreted by a runtime environment called [Node.js](https://nodejs.org/en).

Node is an open-source, cross-platform JavaScript runtime environment that executes JavaScript code outside a web browser. It's a powerful and versatile JavaScript runtime environment, enabling developers to build scalable, high-performance applications.

It uses the same *V8 JavaScript Engine* used in the Chrome browser to compile JS programs into machine code.

Node can be used to build a variety of applications, including:

- Command-line tools - Tools that run in the terminal or command prompt.
- Chat applications - Applications that allow users to communicate with each other in real-time.
- File system tools - Tools that allow users to interact with the file system.
- Automation scripts - Scripts that automate tasks like building a project, running tests, etc.
- Web servers - Servers that serve web pages and/or web APIs.

Open-source libraries called packages extend Node’s functionality. Node's package ecosystem is the largest open-source ecosystem in the world.

### Node.js vs. Browser JS

Node's runtime environment for JavaScript is different than that in the browser, primarily because:

- It doesn’t have a browser’s DOM or [Web APIs](https://developer.mozilla.org/en-US/docs/Web/API).
- Node has low-level networking and file system APIs that the JavaScript browser does not (for security reasons).

Let's test this out. Open your web browser's console and type the following:

```js
window;
```

We can see that we have the window object being returned. Now, let's try this in Node. Open your terminal and type the following:

```bash
node
```

Once in the Node REPL, type the following:

```js
window;
```

We can see that we get a `ReferenceError` because the `window` object is not defined in Node. This means we cannot access the DOM or Web APIs in Node. So, lines of code like the following will not work in Node:

```js
document.querySelector('h1');
```

Just like how the `window` object is not defined in Node, some objects or modules that come with Node are not accessible in the browser. Back in your browser's console, type the following:

```js
fs;
```

We can see that we get a `ReferenceError` because the `fs` module is not defined in the browser. Now, let's try this in your Node REPL. Type the following:

```js
fs;
```

What is returned is the `fs` module. This means we can access the file system in Node. Other built-in modules in Node will help with other tasks.

> 📚 [*fs*](https://nodejs.org/api/fs.html) is the built-in Node module for interacting with the file system.

## Review Questions

1. What is Node?
2. What is the difference between Node and browser JavaScript?
3. True or false: This line of code will work in your Node REPL: `window.alert('Hello World!');`.