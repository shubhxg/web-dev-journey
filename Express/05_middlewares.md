## Middlewares

- Middlewares are used to do prechecks before the request reaches the route handler.
- Prechecks should be done before reaching our backend code exposed which is in routehandlers.
- There are basically 2 prechecks done mostly:
    - Auth
    - Input validation
- A middleware directs the control of the js thread to the next middleware or routehandler with `next()` method.
- A middleware takes `req, res, next` as param
- Each route method such as `app.get()`, `app.post()`, etc, takes a range of `middlewares` before actually reaching the route handler. Basically a middleware sits between the route and the route handler.
- You can also do rate limiting using a middleware. You can ensure that the incoming requests are less than a specific number per second.
- `app.use()` is a very powerful method which ensures that middleware given as argument to this method is applied to all the route.
- So we can do something like this: `app.use(express.json());`this ensures that before reaching each route the middleware is applied to all of them.

## Types of middleware on basis of functionality

1. Preprocessing: `body-parser`, `express.json`, `zod`
2. Auth: 
3. Error handling: `Global catch`
4. Logging: `morgan`

## Types of middlewares on basis of usage

1. Built in 
2. Custom 
3. Third party

## Using middlewares globally

We can use `.use()` method to use middlewares globally.
This middleware will be applied to all the endpoints.

```jsx
app.use(middleware);
```