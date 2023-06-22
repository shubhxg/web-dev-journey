# Everything about APIs

APIs are the building blocks of modern software because they allow sharing of resources and services across applications, organizations, and devices.

## Why are APIs important?

- Brings important features such as automation.
- No need to create the wheel again just use the API.
- APIs can be products themselves.

> For example: Software as a Service (SaaS) products like Stripe's payment APIs or Twilio's text messaging and email APIs.

## Real world example of API

![real world example](https://github.com/shubhsharma19/web-development-notes/assets/69891912/c43f3ac7-1c35-4b6e-8aba-fea058367490)


A customer who wants food doesn’t go into the kitchen to cook. They don't even have to know how to make the food! They only have to ask the **waiter** for the food, and waiter will bring the food.

Here waiter is an example of **API**, customer is **client**, and kitchen is **server**.

## Types of APIs

- **Hardware APIs:** Interface for software to talk to the hardware.

Example: How your phone's camera talks to the operating system.

- **Software Library APIs:** Interface to directly consume code from another code base.

Example: Using methods from a library you import into your application.

- **Web APIs:** Interface to communicate across code bases over a network.

Example: Fetching current stock prices from a finance API over the internet.

## Types of API on the basis of Accesibility

- **Public:** Available for everyone
- **Private:** Not for everyone, only used within a specific organization
- **Partnered:** Consumed between one or more organizations

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

## What is Rest API

![Rest API Diagram](https://github.com/shubhsharma19/web-development-notes/assets/69891912/0888b654-7ded-43ae-a8ed-8869be57c923)

- lmagine you have a **vending machine**. When you press the buttons, it performs certain actions and gives you the desired item. Now, think of the vending machine as a **server**, and you as a **client** who wants to interact with it.
- A **REST API** is like a set of rules that the vending machine and you follow to communicate with each other. It defines how you can ask the server for specific items and how the server responds to your requests.
- In this case, the vending machine has different buttons **(endpoints)** representing different items **(resources)** you can get. For example, there might be a button for snacks, drinks, or candies. Each button has a unique label **(URL)** that tells the vending machine what you want.
- To get the item you want, you press the corresponding button **(send an HTTP request)** to the vending machine. The machine understands the request and performs the necessary action **(GET, POST, PUT, DELETE, etc).** It may give you the item you requested **(response)** or perform some other action based on your request.
- The vending machine is **"stateless",** meaning it doesn't remember anything about your previous requests. Each time you press a button, you provide all the necessary information for the machine to understand what you want. This is because HTTP is a **Stateless protocol**.
- Similarly, in a REST API, the server and client (which could be a website or mobile app) interact using standard rules. The client sends requests to the server's specific URLs (endpoints) to get or manipulate data. The server understands the requests and responds accordingly, providing the requested information or performing the requested actions.
- REST APIs are widely used in web development to create services that allow different systems and applications to communicate and exchange data.

## Request methods

![request methods](https://github.com/shubhsharma19/web-development-notes/assets/69891912/2527f6f2-d662-45c5-9281-818b3b679175)

When we make an HTTP call to a server, we specify a **request method** that indicates the type of operation we are about to perform. 

These are also called **HTTP verbs**.

Here are some commonly used status codes (CRUD operations):

- **GET:** Used to retrieve data (Read)
- **POST:**	Used to send data (Create)
- **PUT/PATCH:** Used to update data (Update), PUT usually replaces an entire resource, whereas PATCH usually is for partial updates
- **DELETE:** Used to delete data (Delete)

## Status Codes
Status codes are the indicators of whether a request failed or succeeded.

Status codes are **three-digit numbers** that are returned by servers as a response. They provide information about the status of the request and helps communicate the outcome of the request to the client.

**Here are some commonly encountered status codes:**

![200](https://github.com/shubhsharma19/web-development-notes/assets/69891912/9bcf2879-a954-4848-b8e3-e053d5a77249)

![300](https://github.com/shubhsharma19/web-development-notes/assets/69891912/74aee074-f467-4fd7-a0ad-978c58736f6b)

![400](https://github.com/shubhsharma19/web-development-notes/assets/69891912/1c654c79-766b-4d7d-b663-a3c4dc52eeda)

![500](https://github.com/shubhsharma19/web-development-notes/assets/69891912/fc048d47-ed51-41ed-aecd-0ea13a5de5ff)

## How to make a Request

When computers communicate with each other over a network, they follow a pattern called **the request-response pattern**. 

Imagine you want to get information from a server. You send a request to the server asking for that information, and then the server processes your request and sends a response back to you.

In this case, I used a tool called **Postman**, which acts as the **client**. 

A client is like a messenger that sends requests on your behalf. It could be a web browser or an application you have created.

To know which method to use, always read the documentation for the API you're working with!

In addition to a request method, a request must include a **request URL** that indicates *where* to make the API call.

A request URL has three parts: 

- **protocol** (**`http://`** or **`https://`**),
- **host** (location of the server)
- **path**
  
> In REST APIs, the path often points to a reference entity, like "books".

![apiresponse](https://github.com/shubhsharma19/web-development-notes/assets/69891912/c6f46ef3-44f2-433f-900b-a4301a2219b3)

Here I made a specific type of request called an **HTTP GET** request. I asked for the information from a server using the address `https://library-api.postmanlabs.com/books`

The server received my request and understood that I wanted to get a list of books. It processed my request and generated a response. Then it sent that response back to the Postman client installed in my laptop.

In the end, I received the response from the server, which contained the list of books requested.

So, **the request-response pattern** is like a conversation between a client and a server. The client asks for something, and the server provides the requested information in the response. It's a way for computers to exchange data and communicate over a network.

## Query parameter syntax

Query parameters are added to the end of the path. They start with a question mark **`?`**, followed by the key value pairs in the format: `key=value` 

For example, following request might fetch all photos that have landscape orientation:

`GET https://some-api.com/photos?orientation=landscape`

If there are multiple query parameters, each is separated by an ampersand sign `&`

`GET https://some-api.com/photos?orientation=landscape&size=500x400`

Here, two query parameters to specify the orientation and size of photos to be returned.

`https://www.google.com/search?q=postman`

This request adds a search term as a query parameter `q=postman` ("q" refers to "query" here) to the `GET /search` path on Google's server.

## When to use query parameters?

The answer is always read the **API documentation** first before using it.

Sometimes query parameters are optional and allow you to add filters or extra data to your responses. Sometimes they are required in order for the server to process your request. APIs are implemented differently to fulfill different needs and this is why its suggested that we always read the documentation first.

## Path Parameters

Another way of passing request data to an API is via **path parameters**. 

A path parameter (path variable) is a dynamic section of a path, and is often used for IDs and entity names such as usernames.

Path parameters come immediately after a slash in the path. For example, the [GitHub API](https://docs.github.com/en/rest/reference/users#get-a-user) allows you to search for GitHub users by providing a username in the path in place of **`{username}`** below:

`GET https://api.github.com/users/{username}`

Making this above API call with a value for username will fetch data about that user.

You can also have multiple path parameters in a single request, such as this endpoint for getting a user's GitHub code repository:

`GET https://api.github.com/repos/{owner}/{repoName}`
