## Creating custom middlewares example:

We can create custom middlewares and then put them before the route handler callback.

```jsx
app.METHOD('/ROUTE', customMiddleware, (req, res) => {
  // route handler code
})
```

### For example:

```jsx
// middleware to check user auth
const userMiddleware = (req, res, next) => {
	const { username, password } = req.header;
	if(!(username === something && password === something)) {
		res.status(403).json({error: "error"})
	} 
	next();
}

// middleware to check kidneys
const idMiddleware = (req, res, next) => {
	const { id } = req.params;
	if(!(id >= 1 && id <= 2)) {
		res.status(403).json({error: "error"});
	}
	next();
}

// using middleware here 
app.METHOD('route', userMiddleware, idMiddleware, (req, res) => {
	// do something here
	res.json({})
})
```

## Using custom middleware globally

```jsx
app.use(userMiddleware, idMiddleware);
```