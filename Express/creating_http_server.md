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
- `const app = express();` creates an instance ofthe express application using express()
- `const port = 3000;` this line assigns the 3000 to port which will be used to bind with the local server you are creating, i,e. `localhost:3000`
- `app.get('/', () => { res.send('Helloworld!') })` This line defines a route handler for the HTTP GET method. So that when a request is made to root path ('/'),
  the callback specified in the second argument is executed.
- `app.listen(port)` this line starts the server and makes it listen on the port. Now the server is ready to handle incoming requests.


## Why port 3000?
- Port 3000 is commonly used as a default port for running local development servers. 
- When you run a web server on your machine, it needs to bind to a specific port to listen for incoming HTTP requests.
- Port 3000 is often chosen because it is one of the so-called **"unprivileged"** ports (ports numbered from 0 to 1023 are 
considered privileged and require special permissions to be used by regular users).
- Developers frequently use port 3000 for local development environments because it's easy to remember and less likely to conflict with 
other services that might be running on the same machine.
- However, it's important to note that you can choose a different port if 3000 is 
already in use or if you prefer a different one.
