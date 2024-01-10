# ![Intro to Node - Intro to NPM](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will understand the fundamental roles and capabilities of Node Package Manager (NPM) in Node.js development

## Introduction to NPM - Node.js' essential tool

Node Package Manager (NPM) is an indispensable tool in the Node.js ecosystem, primarily used for initializing and managing dependencies in Node applications. 

### What is NPM?

NPM is primarily a [package manager for Node.js](https://nodejs.org/en/learn/getting-started/an-introduction-to-the-npm-package-manager). It serves as a command-line utility that aids in setting up, managing, and maintaining Node.js projects, but it is also so much more.

**NPM can:**

1. **Initialize Node.js Projects**: 
   - NPM is used to initialize new Node.js projects. The command `npm init` creates a `package.json` file, which acts as the blueprint of your project, storing crucial information like project metadata and dependencies.

2. **Install Packages**: 
   - NPM allows you to install third-party packages and libraries into your Node.js project. By using commands like `npm install <package-name>`, you can add new functionalities to your project with ease.
   - It handles the installation of both local dependencies (specific to a project) and global dependencies (available across all Node.js projects on a system).

3. **Manage Dependencies**: 
   - NPM effectively manages the versions of various packages your project depends on, ensuring compatibility and smooth functioning. The dependencies are tracked in the `package.json` file, allowing for easy updates and consistent environments across different setups.


> 📚 NPM is not just a tool but an integral part of the Node.js ecosystem, streamlining development and facilitating efficient project management.


## The NPM ecosystem

In our previous lessons, we discussed Node modules and their role in building efficient, reusable code within Node.js. Shifting our focus, we now explore NPM not just as a tool, but as a key entry point into the expansive Node.js ecosystem. NPM opens up a world of possibilities, granting access to an extensive library of external code packages available at npmjs.com, the public registry for Node.js packages.

### What does [npmjs.com](https://www.npmjs.com/) offer?

- **A Registry**: NPM hosts over 1.3 million packages, offering a wide range of solutions, from utilities to frameworks. 
- **Packages**: A Node package is a piece of code that someone else has written and published to a public registry. This package can then be easily used in your own Node.js projects, allowing you to leverage pre-built functionality without having to write the code from scratch.
  - **Example**: The [Express](https://www.npmjs.com/package/express) package, combines modules to facilitate the creation of web servers
- **Community:** NPM is not just for installing external packages; it's also a platform for publishing your own packages, thereby contributing to the Node.js community.