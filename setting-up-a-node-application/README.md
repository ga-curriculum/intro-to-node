# ![Intro to Node - Setting up a Node Application](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to set up a basic Node.js application.

## Setting up your first Node.js application

After learning about Node.js and its package ecosystem, let's dive into setting up a Node.js application and preparing it to use Node packages.

### Initializing a Node.js project

1. **Creating the Base**: Navigate into your newly created `intro-to-node` directory. This will serve as the foundation for your Node app. 

2. **Project Initialization**:
   - Run the following command in your project's root directory:
     ```bash
     npm init
     ```
   - This initializes your project, prompting you to fill in details like project name and version. For a quick setup, you can simply press enter to accept each of the default values.

3. **Quick Initialization**:
   - Alternatively, use:
     ```bash
     npm init -y
     ```
   - This automatically accepts all default values without prompting. 
   
   > The result of this set up sequence is the creation of a `package.json` file in your project. We can see some of the default values we accepted included in this file. For example, the `name` of our project is `intro-to-node`, and the `version` is `1.0.0`.


## Understanding `package.json`

Think of `package.json` in your Node.js project like a card catalog in a library. Just as a card catalog keeps a record of all the books and their locations, `package.json` keeps track of all the NPM packages (*dependencies*) you have installed into your application, along with other important project information.

**Primary purpose:**

- **Lists Project Metadata**: Contains details like your project's name, version, and entry point.
- **Lists Dependencies**: It lists all the external packages your project needs to function.

>📚 A *dependency* is an external library or module essential for your project's functionality. When you install a package and use its methods in your code, your application relies on that package to operate correctly, hence the term 'dependency.' Dependencies offer pre-built functions, making development more efficient and reducing the need to write duplicate code.

### `npm install`

-  By running `npm install`, all dependencies listed in `package.json` are automatically downloaded. This ensures that every developer working on the project has the exact tools needed, without the overhead of transferring numerous files.
