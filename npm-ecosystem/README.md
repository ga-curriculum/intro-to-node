# ![Intro to Node - NPM Ecosystem](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to explore the ecosystem of Node Package Manager (NPM).


Now that you've created and used modules of your own let's see how we can install open-source packages and use the modules they contain.


## Node Package Manager (NPM)

Node uses a package management system to distribute open-source packages called **N**ode **P**ackage **M**anager (*npm*). Usually, a package distributes a Node module, however, sometimes the package distributes a CLI instead of a module we would use in our program.

> 📚 *npm (Node Package Manager)*  is the default package manager for Node.js, which allows developers to easily install, update, and manage third-party libraries, and dependencies for their JavaScript projects.

The Node Package Manager is an integral part of the Node.js ecosystem, serving as a package registry and command-line tool for managing JavaScript packages. It enables developers to easily find, install, share, and update open-source software packages, simplifying the process of building applications with Node.js.

At the heart of npm lies a vast public registry, home to over 1.3 million open-source JavaScript packages. This centralized repository serves as a treasure trove of software components, readily accessible to developers seeking to enhance their applications. Whether you require a simple utility library or a complex framework, the npm registry has something to offer.

## `package.json` and `npm init`

Node programs use a **`package.json`** file that tracks the installed modules that the app depends upon. Tracking an application’s dependencies in **`package.json`** removes the necessity to push the app’s node modules to the projects GitHub repo - this saves **MASSIVE** file storage and bandwidth.

If you start a Node app from scratch, the first thing you should do is create the **`package.json`** file by entering the following command:
```bash
npm init
```

It’s okay to accept all of the default settings - to do so without being prompted, you can run this command:

```bash
npm init -y
```

