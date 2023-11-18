# ![Intro to Node - npm Practice](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will practice installing node packages.

## Intalling the package

To get some extra practice installing npm packages, we're going to install a package called [`prompt-sync`](https://www.npmjs.com/package/prompt-sync). `prompt-sync` provides a simple and efficient way to handle user input in Node.js scripts.

Install the package using the following command:

```bash
npm i prompt-sync
```

To recap, this command will download and install the `prompt-sync` package into our project's `node_modules` directory.

## Importing the module

Once the package is installed, we need to import it into our Node.js script:

```js
const promptSync = require('prompt-sync')
const prompt = promptSync()
```

Consulting [the documentation for prompt-sync](https://www.npmjs.com/package/prompt-sync) reveals that `require('prompt-sync')` will return a function that itself generates a function that we can use.  The reason for this function generation gets into the details of some of the extended functionality of prompt-sync, and it's not really worth going into those at the moment.  For now, just run the code in the default manner described above.
## Using prompt-sync

Having completed the code above, we now have a `prompt` function we can use to easily get user input.  Let's use it to prompt the user for their name:

```js
const name = prompt('What is your name? ')
console.log('Hello, ' + name + '!')
```

This code prompts the user for their name using the `prompt()` function, stores the input in the `name` variable, and then greets the user using their provided name.

## Handling user input with conditional statements

We can also utilize user input to control the flow of our program using conditional statements. For instance, to ask the user if they like pizza and respond accordingly:

```js
const likePizza = prompt('Do you like pizza? (yes/no) ');

if (likePizza === 'yes') {
  console.log('Great! I love pizza too!');
} else {
  console.log('Too bad. Pizza is delicious!');
}
```

This code prompts the user if they like pizza, stores their response in the `likePizza` variable, and then uses an `if-else` statement to provide a different response based on their input.

## Exploring `prompt-sync` documentation

The `prompt-sync` module offers additional features beyond basic user input, such as prompting with default values, hiding user input, and customizing input validation. To fully explore its capabilities, refer to the module's documentation for detailed explanations and usage examples.