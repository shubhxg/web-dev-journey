## What the hell is promises and why we needed it?

In JavaScript, as in many other programming languages, tasks often involve async operations. 

These are operations that don't necessarily happen immediately and may take some time to complete. Examples include fetching data from a server, reading a file, converting data into JSON, or waiting for a user to click a button.

Before promises were introduced, managing asynchronous operations was often done using callbacks. 

**Callbacks** are functions that are passed as arguments to another function and are executed later, once the asynchronous operation is complete. 

However, as programs grew in complexity, managing callbacks became challenging, leading to what's often referred to as **"callback hell" or "pyramid of doom."** 

This is a situation where nested callbacks make the code hard to read and maintain.

Promises were introduced to address these issues and provide a cleaner way to handle asynchronous operations. 

## So what is Promise?

A promise is an object representing the **eventual completion or failure of an async operation** and its resulting value. 

It has three states: **pending, resolved (fulfilled), or rejected.**

## Basic example to understand

```jsx
// Creating a promise 
let myPromise = new Promise((resolve, reject) => {
    // Simulating async operation using setTimeout, but could be anything
    setTimeout(() => {
        let success = true;
        if (success) {
            resolve("Data fetched successfully");
        } else {
            reject("Error fetching data");
        }
    }, 2000);

// Consuming the promise
myPromise
.then((result) => {
	console.log(result);
})
.catch((error) => {
  console.error(error);
})
//default one, gets executed no matter resolve or reject
.finally(() => {}); 
```

## Handling data with multiple then and catch → Chaining

```jsx
const promiseFour = new Promise((resolve, reject) => {
	setTimeout(() => {}
		//fake error created
		let error = false;

		console.log("Async task completed!");
		//response returned with resolve 
		if(!error) resolve([1,2,3]);
		//error returned with reject
		else reject("Error!");
, 1000);
});

promiseFour.then((response) => {
	return response;
})
.then((response) => {
	console.log(response.flat(''));
})
.catch((err) => {console.log(err)})

// default one -> always gets executed
.finally(() => {});
```