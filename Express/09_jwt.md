## Use of JWT and more

> For nodejs ⇒ https://github.com/auth0/node-jsonwebtoken

How do you ensure that your user has access to the certain resources of your website.

- Answer: **authentication.**

### Dumb way

Create a custom middleware to check every time user sends their id, password, username, email etc. depending on your needs. this can be done like `app.use(authMiddleware());`

### A better way

1. send the user a token on signup/signin
2. ask user to send back the token in all future requests
3. ask user to forget the token when logout

Inside the `app.get()` we will send a middleware to generate a token and also check if the user has the token. Now each time when user sends a request server checks the token. so `app.use(tokenCheckerMiddleware)`

---

## What is JWT?

Just like encryption of data, It is a compact, URL-safe means of representing `claims` between two parties. 

The claims are typically used to transmit information about an `authenticated` user or other information between parties in a web application.

JWTs are often used for `authentication and authorization in web applications.` When a user logs in, a server can generate a JWT and send it to the client. 

The client can then include the JWT in the headers of next requests to authenticate itself.

The server can verify the integrity of the JWT.

A JWT consists of three parts: Header, payload and secret key.

## Local storage

This is a place in browser where the token is stored for auth, you can find it in the browser → `application → local storage, storage → local storage.`

Once you logout then token is removed.

Frontend → backend → DB

---

## Working with JWT in Express

```jsx
const jwt = require('jsonwebtoken');

// secret or private key used to sign the token. 
// This key is essential for verifying the authenticity of the token later.
const jwtPass = '12345';

app.post('/signin', (req, res) => {
  const { username, password } = req.body;

// if user does not exist
  if(!userExists(username, password)) {
    return res.status(403).json({
      message: "User does not exist"
    });
  }
	// user exists, creating a token
  const token = jwt.sign({ username }, jwtPass, { expiresIn: '24h' });

	// returning token to the user
  return res.status(200).json({
    message: "Signin successful!",u
    token
  });
})

// Middleware for token verification
const tokenCheckerMiddleware = (req, res, next) => {
  const token = req.headers.authorization;
  if (!token) {
    return res.status(403).json({ message: "A token is required for authentication" });
  }
  try {
    // Verification of user
    const decoded = jwt.verify(token, jwtPass);
    req.user = decoded; // Attaching the decoded user to the request
    next(); // Proceed to the next middleware/function
  } catch (err) {
    return res.status(401).json({ message: "Invalid Token" });
  }
};

// Example of using the middleware
app.get('/someProtectedRoute', tokenCheckerMiddleware, (req, res) => {
  // If the request reaches here, the user is authenticated
  res.send('Access granted to protected content');
});
```

Explanation 

- to create a token → `const token = jwt.sign({ username }, jwtPass)` Here the `sign()` method is used with the payload `{ username }` which is converted to the token and `jwtPass` is the secret key which is used to verify the token
- now to verify the token with the username→ `const decoded = jwt.verify(token, jwtPass); const username = decoded.username;`