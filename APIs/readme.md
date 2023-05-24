# Everything about APIs

APIs are the building blocks of modern software because they allow sharing of resources and services across applications, organizations, and devices.

## Why are APIs important?

- Brings important features such as automation.
- No need to create the wheel again just use the API.
- APIs can be products themselves.

> For example: Software as a Service (SaaS) products like Stripe's payment APIs or Twilio's text messaging and email APIs.

## Real world example of API

A customer who wants soup doesn’t go into the kitchen to cook. They don't even have to know how to make soup! They only have to know *how to ask* \*the **waiter\*** for soup*,* and expect the waiter will bring back soup*.*

Here waiter is an example of API, customer is client, and kitchen is server.

## Types of APIs

- Hardware APIs: Interface for software to talk to the hardware.

Example: How your phone's camera talks to the operating system.

- Software Library APIs: Interface to directly consume code from another code base.

Example: Using methods from a library you import into your application.

- Web APIs: Interface to communicate across code bases over a network.

Example: Fetching current stock prices from a finance API over the internet.

## Types of API on the basis of Accesibility

- Public: Available for everyone
- Private: Not for everyone, only used within a specific organization
- Partners: Consumed between one or more organizations

---

## Let's talk about CORS

- CORS stands for **Cross-Origin Resource Sharing.**
- Allows web pages to access resources from other domains.
- Useful for things like embedding images, videos, and scripts from other websites.
- Without CORS, web pages would be limited to only accessing resources from the same domain
- CORS uses a set of **HTTP headers** to communicate between the browser and the server.
- The browser sends a request to the server with the CORS headers. The server then responds with a response that indicates whether or not the request is allowed.
- If the request is allowed, the browser will load the resource from the server. But if not, then the browser will not load any resource.

## How CORS work?

1.  A web page makes a request to a server for an image.
2.  The browser sends a CORS header with the request.
3.  The server responds with a response that indicates whether or not the request is allowed.
4.  If the request is allowed, the browser will load the image.
5.  If the request is not allowed, the browser will not load the image.

## Benefits of CORS

- It allows web pages to access resources from other domains.
- It can be used to improve the performance of web pages by caching resources.
- It can be used to improve the security of web pages by preventing cross-site scripting attacks.

## Drawbacks

- It can be complex to configure.
- It can introduce security vulnerabilities.

## Why use Postman?

We can either use `curl` or we can use postman. However, postman has a better interface to build and consume APIs.

For example: `curl url` This command will fetch the data about that URL. But this will put all the data on the screen, instead use Postman.
