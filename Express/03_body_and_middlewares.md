## Parsing in context of web development
Parsing in context of web development basically means extracting information from the data of http req or response in form of json etc.

## Body of the request
You need to ensure that the `HTTP request` body has been `parsed` into a usable format, such as JSON or URL-encoded form data. 

When an HTTP request is sent, the data in the body, whether it's form data, JSON, or other content is transmitted as a stream of bytes. This raw format isn't immediately usable within your application code.

This is where middleware steps in to bridge this gap. It intercepts incoming requests before they reach your application logic and performs the necessary transformations on the request body.

## Middlewares
Middleware uses parsing functions or libraries to decode the raw bytes based on the request's content type. 
- For JSON data, it uses a JSON parser to convert the bytes into a JavaScript object.
- For form data, it parses the key-value pairs into an object or array.
- For other content types, it might apply specific decoding mechanisms as needed

Once the parsing is complete, middleware makes the parsed data accessible within your code. 

In frameworks like Express.js, the parsed data is typically attached to the req.body object, allowing you to easily work with it in your request handlers.