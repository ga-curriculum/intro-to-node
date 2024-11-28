<h1>
  <span class="headline">Intro to Node</span>
  <span class="subhead">Intro to npm</span>
</h1>

**Learning objective:** By the end of this lesson, students will understand the role of Node Package Manager (npm) in Node development.

## Introduction to npm

Node Package Manager (npm) is an indispensable tool in the Node ecosystem, primarily used for installing and managing dependencies in Node apps.

### What is npm?

npm is a [package manager for Node](https://nodejs.org/en/learn/getting-started/an-introduction-to-the-npm-package-manager). It's a command-line utility that aids in setting up, managing, and maintaining Node projects, but it is also more. On the command line, npm is used to:

1. **Initialize Node projects**: npm is used to start new Node projects.
2. **Install packages**: npm lets you install third-party packages and libraries into your Node project. It handles the installation of local dependencies (specific to a project) and global dependencies (available across all Node projects on a system).
3. **Manage dependencies**: npm manages the versions of various packages your project depends on, ensuring compatibility and functionality.

## The npm ecosystem

npm is not just a command-line tool but also an extensive library of external code packages available at [npmjs.com](https://npmjs.com), the public registry for Node packages.

### What does [npmjs.com](https://npmjs.com/) offer?

npm hosts over 1.3 million Node packages in their *registry*.

These are applications that other developers have written and published to `npm`. Many kinds of apps are available, from small utilities to massive frameworks. Here are a couple of examples:

- **[validator](https://www.npmjs.com/package/validator)**: Used to help validate string data. For example, it can be used to confirm that a string is formatted as a email address.
- **[Express](https://www.npmjs.com/package/express)**: Facilitates the creation of web servers.

npm is not just for installing external packages; it's also a platform for publishing your own packages to contribute back to the Node community.

> 📚 A software *registry* is a centralized service that stores packages, libraries, or modules, allowing developers to publish, share, and access reusable code components.
