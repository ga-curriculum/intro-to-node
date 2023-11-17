# ![Intro to Node - NPM Ecosystem](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to explore the ecosystem of Node Package Manager (NPM).
## Node Package Manager (NPM)

In addition to its own built-in modules like `fs`, node easily allows other developers to build their own modules that extends Node's capabilities.  These modules are called packages.

Node uses a package management system to distribute and easily install open-source packages called **N**ode **P**ackage **M**anager (*npm*). Usually, a package is a Node module that you can use in your own code (similar to `fs`), however, sometimes the package is a CLI tool that you run in your terminal.

The Node Package Manager is an integral part of the Node.js ecosystem.  It is both a command-line tool for managing JavaScript packages on your own computer as well as a way to distribute packages that you write. It enables developers to easily find, install, share, and update open-source software packages, simplifying the process of building applications with Node.js.

At the heart of npm lies a vast public registry, home to over 1.3 million open-source JavaScript packages. This centralized repository serves as a treasure trove of software components, readily accessible to developers seeking to enhance their applications. Whether you require a simple utility library or a complex framework, the npm registry has something to offer.
## Creating a node app

When starting a Node app from scratch, the first thing you should do is initialize the project:

```bash
npm init
```

This will give you a series of prompts.  For now just hit `Enter` for each of them.  To accept all of the default settings without being prompted, you can run this command:

```bash
npm init -y
```

In either case, you'll now see that `npm` has created a `package.json` file.  Node programs use this file to track the installed modules that the app depends upon. Tracking these dependencies in `package.json` removes the necessity to push the app’s npm modules to the project's GitHub repo - this saves **MASSIVE** file storage and bandwidth.  When we `git clone` someone else's project for the first time, Git will download all of the code that the developer wrote without the npm modules that they installed themselves.  We can then use a single `npm` command to easily install these packages ourselves (more on this later).