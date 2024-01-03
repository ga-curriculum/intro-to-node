# ![Intro to Node - What is Node?](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be introduced Node.js and its significance.

## What is Node.js?

JavaScript can be interpreted by a couple of different environments. The most common environment is the browser. However, JavaScript can also be interpreted by a runtime environment called [Node.js](https://nodejs.org/en).

Node.js is an open-source, cross-platform JavaScript runtime environment that executes JavaScript code outside of a web browser. It's a powerful and versatile JavaScript runtime environment, enabling developers to build scalable, high-performance applications.

It uses the same *V8 JavaScript Engine* used in the Chrome browser to compile JS programs into machine code.

Node.js can be used to build a verity of applications, including:

- Command-line tools - Tools that run in the terminal or command prompt.
- Chat applications - Applications that allow users to communicate with each other in real-time.
- File system tools - Tools that allow users to interact with the file system.
- Automation scripts - Scripts that automate tasks, such as building a project, running tests, etc.
- Web servers - Servers that serve web pages and/or web APIs.

Open-source libraries called packages extend Node.js’s functionality. Node.js's package ecosystem is the largest open-source ecosystem in the world.

### Node.js vs. Browser JS

Node.js's runtime environment for JavaScript is different than that in the browser, primarily because:

- It doesn’t have a browser’s DOM or [Web APIs](https://developer.mozilla.org/en-US/docs/Web/API).
- Node.js has low-level networking and file system APIs that browser JavaScript does not (for security reasons).

Let's test this out. Open your web browser's console and type the following:

```js
window
```

We can see that we have the window object being returned. Now, let's try this in Node.js. Open your terminal and type the following:

```bash
node
```

Once in the Node.js REPL, type the following:

```js
window
```

We can see that we get a `ReferenceError` because the `window` object is not defined in Node.js. This means we are unable to access the DOM or Web APIs in Node.js. So lines of code like the following will not work in Node.js:

```js
document.querySelector('h1')
```

Just like how the `window` object is not defined in Node.js, there are some objects or modules that come with Node.js that are not accessable in the browser. Back your browser's console, type the following:

```js
fs
```

We can see that we get a `ReferenceError` because the `fs` module is not defined in the browser. Now let's try this in your Node.js REPL. Type the following:

```js
fs
```

What is returned is the `fs` module. This means we are able to access the file system in Node.js. There are other built in modules in Node.js that will help in other tasks.

> 📚 [*fs*](https://nodejs.org/api/fs.html) is the built-in Node.js module for interacting with the file system.

## Reivew Questions

1. What is Node.js?
2. What is the difference between Node.js and browser JavaScript?
3. True or false: This line of code will work in your Node.js REPL: `window.alert('Hello World!')`.