## Using express to create a basic http server
```jsx
const express = require('express');
const app = express();
const port = 3000;

// since we are sending data to the client so we used get method
app.get('/', (req, res) => {
	res.send('Helloworld!')
});

app.listen(port);
```

## Let's break it down and understand how it works
- `const express = require('express');` This line imports the Express and assigns it to the express variable, require() is a Node.js function used to import modules.
- `const app = express();` creates an instance ofthe express application using express() method
- `const port = 3000;` this line assigns the 3000 to port which will be used to bind with the local server you are creating, i,e. `localhost:3000`
- `app.get('/', () => { res.send('Helloworld!') })` This line defines a route handler for the HTTP GET method. So that when a request is made to root path ('/'),
  the callback specified in the second argument is executed.
- `app.listen(port)` this line starts the server and makes it listen on the port. Now the server is ready to handle incoming requests.

## Request and Response
- A request from the user contains all the information such as header, query param, body, etc.
- Generally a request and response is sent as param to the callback in the route handler, eg: `(req, res) => {}`
- In order to read the header from the request you can use either `rawHeaders` or `headers` property of the request.
- Server can send anything back to the user using response. eg: `res.send('Hello world!')`
- By default client side sends a get request to get the html document from the server.

## What is an endpoint?
The URL is composed of several components, and the endpoint is typically identified by the path or resource name specified in the URL.
For example: `/home` or `/about` etc.

## Why port 3000?
- Port 3000 is commonly used as a default port for running local development servers. 
- When you run a web server on your machine, it needs to bind to a specific port to listen for incoming HTTP requests.
- Port 3000 is often chosen because it is one of the so-called **"unprivileged"** ports (ports numbered from 0 to 1023 are 
considered privileged and require special permissions to be used by regular users).
- Developers frequently use port 3000 for local development environments because it's easy to remember and less likely to conflict with 
other services that might be running on the same machine.
- However, it's important to note that you can choose a different port if 3000 is 
already in use or if you prefer a different one.
- 1 port works for 1 application/process only.