# Restart Your Web Application

Node.js serves the same code consistently until it is restarted. This prevents inadvertent changes to the application files while the server is up and running. This is also why your message did not change.

1. In the Terminal in Visual Studio Code, stop your Node.js application by pressing `Control-C` (which works on both Mac and Windows).

2. Restart your application by typing the following into the Terminal:

```
node hellonode.js
```

3. Return to your web browser and refresh the page. You will now see your *new* message returned to the browser.