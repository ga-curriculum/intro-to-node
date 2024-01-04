# ![Intro to Node - NPM Ecosystem](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to explore the ecosystem of Node Package Manager (NPM).

## Node Package Manager (NPM)

Outside of the built-in modules like `http` or `fs`, Node.js has a vast ecosystem of open-source packages that we can use in our code. These packages are distributed through a package manager called [Node Package Manager (NPM)](https://www.npmjs.com/). Not only does NPM allow us to install packages, but it also allows us to publish our own packages.

At the heart of NPM lies a vast public registry, home to over 1.3 million open-source JavaScript packages. This centralized repository is a treasure trove of software components readily accessible to developers seeking to enhance their applications. Whether you require a simple utility library or a complex framework, the NPM registry offers something.

> 📚 Packages can be one or several modules bundled together. For example, the [Express](https://www.npmjs.com/package/express) package is a collection of modules that allow us to create a web server.

## Creating a node app

During our set-up, we created a folder called `intro-to-node` and a file called `server.js.` This is going to be the base of our first Node application. When starting a Node app from scratch, the first thing you should do is initialize the project:

```bash
npm init
```

This command is going to prompt us for some information about our project. We can hit enter to accept the default values for each prompt. Once complete, NPM will create a `package.json` file in our project. We can see some of the default values we accepted included in this file. For example, the `name` of our project is `intro-to-node`, and the `version` is `1.0.0`.

Alternatively, we can use the `-y` flag to accept all of the default values without being prompted:

```bash
npm init -y
```

The `package.json` file tracks the installed NPM packages that our application depends on. These are called dependencies. Tracking these dependencies in `package.json` removes the necessity to push the app’s NPM modules to the project's GitHub repo - this saves **MASSIVE** file storage and bandwidth. When we `git clone` someone else's project for the first time, Git will download all of the code the developer wrote, minus the NPM modules they installed themselves. We can then use a single `npm` command to install these packages easily (more on this soon).

> 📚 A *dependency* refers to an external library, module, or component that a project relies on to function correctly, providing pre-built functionality or reusable code to simplify development and reduce duplication of effort.

## Review Questions

1. What is NPM?
2. What is a package?
3. What is a dependency?