## Async/Await use

Before the introduction of `async/await`, managing asynchronous operations in JavaScript was primarily done using callbacks and later with promises. 

While promises helped in the **"callback hell"** issue, they still introduced a certain level of complexity, especially when dealing with multiple asynchronous operations in sequence.

**Asyn/await** was introduced to make working with async code even more readable. It provides a syntax that looks and behaves like synchronous code, making it easier for developers to reason about and write asynchronous code.

It is built on top of Promises and is compatible with all existing Promise-based APIs.

## How it works
An async function is declared by prefixing it with the `async` keyword. It ensures that the returned value is a promise and enables the use of await.

The `await` keyword is used inside an async function to pause the function execution until a promise settles, js thread waits for the result and only after promise is settled then js thread goes forward. 

## Some points to remember 
- `await` only works with Promises and not with callbacks
- `await` doesn't handle errors automatically like promises so we need to use try and catch block for that
- when an async function is called, it returns a new `Promise`, which will be either resolved or rejected
- `await` keyword is only valid inside async functions within regular JavaScript code. It won't work outside async function.
. The purpose of async/await is to simplify the syntax necessary to consume promise-based APIs, and the behavior of async functions is such that they always return a promise.

## Code example: 

```jsx

// function that returns a promise
function fetchData() {
	return new Promise((resolve) => {
		setTimeout(() => {
			console.log("Async task completed!")
			resolve("Data resolved");
		}, 2000);
	})
}

async functionDataFetcher() {
try {
	const result = await fetchdata();
	console.log(result);
} catch(err) {
	console.log(err)
}

functionDataFetcher();
```