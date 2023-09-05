# Add Additional Files
The application scaffold created by Express Generator doesn't include all of the files necessary for a modern web application. You should create and edit additional files according to the instructions below in order to prepare your application for future distribution.

(server:expressgen:add_files)=
## Create Additional Files

1. Ensure you are at the root level of your application's directory (you should see files such as `package.json` and `app.js`)
2. Add the additional files with a single command:

```
code .gitignore .env start.js README.md
```

You will not use the `.env` file yet, but it's good practice to create it now. Read on to learn how to use the other files.

(server:expressgen:gitignore)=
## Edit Your .gitignore File

1. At a minimum, add the following lines to your `.gitignore` file:

```
node_modules
.env
```

This prevents your `node_modules` directory and your .env file from being added to your local Git repository (and, more importantly, from your remote repository too!)

2. For a more robust example of a `.gitignore` file, follow the instructions in the [Git setup section of this workbook](git:init:gitignore)

(server:expressgen:readme)=
## Edit Your README.md File

Your README file uses the [Markdown syntax](https://www.markdownguide.org/basic-syntax/) to add context and notes about the application you are developing. You should add a brief overview of the project here.

```{admonition}  Pro Tip!
If you've used outside references (like articles, tutorials, or blog posts) to help you build your application, update your README with links to the most valuable resources for later reference.
```

(server:expressgen:startjs)=
## Edit Your start.js File

The `start.js` file is a script that allows you to configure your application's launch configuration. It's a good practice to keep this configuration separate from the actual app commands located in `app.js`.

The following is a very common `start.js` file:

```
const app = require('./app');

const server = app.listen(8081, () => {
    console.log(`Express is running on port ${server.address().port}`)
});
```