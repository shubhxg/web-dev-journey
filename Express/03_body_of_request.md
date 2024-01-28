## Parsing in context of web development
Parsing in context of web development basically means extracting information from the data of http req or response in form of json etc.

## Body of the request
You need to ensure that the `HTTP request` body has been `parsed` into a usable format, such as JSON or URL-encoded form data. 

When an HTTP request is sent, the data in the body, whether it's form data, JSON, or other content is transmitted as a stream of bytes. This raw format isn't immediately usable within your application code.

This is where middleware steps in to bridge this gap. It intercepts incoming requests before they reach your application logic and performs the necessary transformations on the request body.