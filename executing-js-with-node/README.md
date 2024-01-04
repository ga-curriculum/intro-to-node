# ![Intro to Node - Executing JavaScript with Node](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to use Node to execute JavaScript.

## Executing JS with Node

Let’s see how Node runs JavaScript programs in the terminal. Type the following JavaScript in `server.js`:

```js
const multiply = (a, b) => {
    return a * b;
};

const product = multiply(5, 8);
    
console.log(product);
```

Press `ctrl` + `(backtick)` to open the integrated terminal in VS Code and type the following to execute what we just wrote in `server.js`:

```bash
node server.js
```

Yep, running a Node app is that easy!