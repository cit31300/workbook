# Install nodemon

`nodemon` is a package that continuously monitors the source files within your application and automatically restarts the Node server when changes are detected.

`nodemon` is intended to be used only during development, so you will install it for development environments only.

1. Install `nodemon`
```
npm install -D nodemon
```

2. Update the `scripts` section of your `package.json` file to allow the use of `nodemon`:

```{code-block} javascript
:name: package.json
:caption: "Sample `package.json`"
"scripts": {
  "start": "node start",
  "dev": "nodemon --watch -e js,json,ejs"
}
```

The `-e` flag tells `nodemon` to restart your application when there are changes to any JavaScript, JSON, or EJS file.

3. Run your application from the command line with the following line:

```
npm run dev
```