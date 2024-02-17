## What is an http protocol?

HTTP is a set of rules that define how information is exchanged between two machines over the internet. 

It is the foundation of data communication on the web and is widely used for fetching resources like **HTML documents, images, style sheets, etc.**

Some other examples of protocols **https, ftp, webrtc, imap, pop3, smtp, dns, tcp/ip, udp.**

## How frontend communicates with backend?

Frontend and backend communication often relies on HTTP protocol. The frontend (client-side) sends HTTP requests to the backend (server-side), and the backend responds with the requested data or performs the requested actions. This interaction is crucial for dynamic web apps where data needs to be exchanged between the user's device and the server.

## What is a server?

A **server** is a computer that serves data to the client device, In easy terms, its a specialized **computer** or **software** that performs specific tasks for clients. It is designed to manage and share resources, respond to requests, and facilitate communication with the client device. 

A server is based upon **request-response** model which means when a client sends a request a server responds.

## What is Frontend?

UI between the user and the machine, everything a user can see, interact with and send information through. Layouts, buttons, visuals, inputs etc. 

Made using → **HTML, CSS, JS, A JS framework or library like react, vue, svelte, etc.**

## What is Backend?

A backend consists of following

1. Server
2. Databases
3. Application (code running on a server)

These 3 work together to send data to the frontend.

Can be made using → **Nodejs, Java, Golang, rust etc.**

## How does front-end communicate with backend

Answer: **Using http protocols**

Frontend <————**(http protocol)** ———> Backend

## HTTP server

Some code that follows http protocols and is able to communicate with client side (browsers, mobile etc.)

Think of it as a calling app on mobile.

In short, client sends an req, server does something with that data, and server responds back to the client.

> Client (request) <———————-> Server (response) 

## When a front-end sends a request to a server it contains following:

1. A Protocol (http/https) : Set of protocols

2. Url/IP/Port: URL is the website name, IP is a unique number given to each device/website on the internet which is in 4 parts of 3 digits x.x.x.x from 0 to 255

3. Route

4. Header and Body: header contains cookies and queries from the user

5. Method

## Server responds with:

1. Response header

2. Response body

3. Status codes

## Methods

A "method" in the request body typically refers to the HTTP method used to make a request to a server. The HTTP methods define the action the client wants to perform on the specified resource. The most common HTTP methods are:

    GET: To get data from a specified resource.
    POST: To submit data to be processed to a specified resource.
    PUT: To update a specified resource with the provided data.
    DELETE: To deletes the specified resource.
    PATCH: Applies partial modifications to a resource.
    HEAD: Similar to GET but only retrieves the headers of the response without the body.
    OPTIONS: Returns the HTTP methods that the server supports for the specified URL.

## Status codes

A status code is a three-digit integer returned by a server in response to a client's request made to a web server. It provides information about the outcome of the request.

- 100 - 199 informational codes
- 200 - 299 **success (200 - ok, success)**
- 300 - 399 redirected (301 - moved permanently)
- 400 - 499 client side error (401 - unauthorised access, **404 - url not found/data not found**)
- 500-599 server side error (500 - server crashed / internal server error)
