# ![Intro to Node - Executing JavaScript with Node](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to use node to execute JavaScript.

## Executing JS with node

Now that you’ve learned how awesome Node is, let’s see how it runs JavaScript programs.

Type the following JavaScript in `server.js`:

```js
const multiply = (a, b) => {
	return a * b
}

let n = multiply(5, 8)
 	
console.log(n)
```

Press `ctrl` + `(backtick)` to open the integrated terminal in VS Code and type the following to execute what we just wrote in `server.mjs`:

```bash
node server.mjs
```

Yep, running a Node app is that easy!