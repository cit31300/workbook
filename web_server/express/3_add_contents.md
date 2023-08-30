# Write and Run an Express File
We will now create a JavaScript file that contains the specifications for an Express application that runs a Node.js webserver. 

1. Copy and paste all of the code below into the `app.js` file:

```
const express = require('express')
const app = express()
const port = 3000

// Define the root route
app.get('/', (req, res) => {
  res.send('Hello World!')
})

// Start the server so it listens for requests
app.listen(port, () => {
  console.log(`Example app listening on port ${port}`)
})
```

2. Save the file

3. With your file saved, go to the command line in the Terminal window and type the following command to start your web server:

```
node app.js
```
You should see a message in the server console (your Terminal window) that reports the server is running and includes an IP address and port.