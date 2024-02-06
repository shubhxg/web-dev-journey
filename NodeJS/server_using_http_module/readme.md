## Creating a basic server using nodejs, http module and url module.

**Let's see the code first**

```jsx
const http = require('http');
const url = require('url');
const PORT = 3000;

const server = http.createServer((request, response) => {
  const pathName = request.url;

  // parsing json into string before sending to client
  const data = JSON.stringify(
  { name: 'John', age: 30, city: 'New York' });

  // setting header for html
  response.setHeader('Content-Type', 'text/html');
  
  if(pathName === '/' || pathName === '/home') {
    response.end("<h1>Hello world!</h1>");
  } else if (pathName === '/about') {
    response.end("<h1>About me</h1>");
  } else if (pathName === '/api') {
    response.setHeader('Content-Type', 'application/json');
    response.end(data);
  } else { 
    response.writeHead(404).end("<h1>404 Not Found</h1>");
  }
});

server.listen(process.env.PORT || 3000, () => {
  console.log('Server is running on ' + (process.env.PORT || 3000));
});
```

## Let’s break down the code

1. importing module `http` and `url` to work with header url header (route basically)
2. creating server with `const server = http.createServer((req, res) ⇒ { });`
3. inside the callback we take url from the request with `const pathName = req.url`
4. next we have data to send back to client and since json needs to be parsed into string so we use `JSON.parse( )` method
5. next we `set header as contenttype to html/text` which allows us to send the html.
6. now we send different data to according to different routes such as `/` or `/about` using if/else conditions. we check `if pathName === /` then send response according to the route
7. `response.end` is equivalent to `response.send` in express, both send somedata to the user
8. `response.writeHead()` is used to send statuscode like `404` here in this case and then we ended that response with html data
9. in the end of code we make the server listen to the port provided `server.listen(PORT)`
