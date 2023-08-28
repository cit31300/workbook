# Write and Run a Node.js File
We will now create a JavaScript file that contains the specifications for a Node.js server. 

1. Copy and paste all of the code below into the `hellonode.js` file:

```
//Load HTTP module
const http = require("http");

//Set the IP address and port for this server
const hostname = '127.0.0.1';
const port = 3000;

//Create HTTP server and listen on port 3000 for requests
const server = http.createServer((req, res) => {
  //Set the response HTTP header with HTTP status and Content type
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World\n');
});

//Have the server listen for requests and create a callback function that returns the IP address and port in the server console
server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```

2. Save the file

3. With your file saved, go to the command line in the Terminal window and type the following command to start your web server:

```
node hellonode.js
```
You should see a message in the server console (your Terminal window) that reports the server is running and includes an IP address and port.