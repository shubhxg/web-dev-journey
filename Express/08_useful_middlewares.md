## Some useful middlewares 

### Middleware for logging: Morgan

`Morgan` is a middleware for Node.js and Express that simplifies the process of logging HTTP requests and errors. It can be used to log requests, errors, and more to the console.

```bash
npm install morgan -g
```

```jsx
const morgan = require('morgan');
// using tiny preset
app.use(morgan('tiny'));
```

## Zod
[Zod](https://zod.dev/) is most popular library for Input validation. Instead of creating our own middleware to precheck the inputs and validate them before they reach the endpoints we can just use Zod library for that.

Zod comes with different methods to ensure different input data needs.

Check the whole docs here: https://zod.dev/

Installation:

```bash
npm install zod -g
```

Working with Zod:

```jsx
const zod = require("zod");

// method can be any method such as string, object, numbers, arrays etc. which you want to validate.
const schema = zod.method();
schema.safeParse(data);
```