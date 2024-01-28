## Global catches

User might send some data which might crash the server, and when the server is crashed it might return data about the server to the frontend.

This is called an exception and should be avoided with error handling middlewares.

One such middleware is `Global catch`. 

A `global catch` is a type of `error based middleware` used for exceptions which ensures that the error is catched before it reaches the user and a proper error response is sent to the user instead of some random data about the server.

```jsx
// introducing global catch inside the code

app.use((err, req, res, next) => {
	res.status(500).json({msg: "error"})
  next();
})
```