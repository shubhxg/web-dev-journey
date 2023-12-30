## Async nature of JS

### What is async and sync
Sync → Together or Sequential but one thing at a time.
Async → Parallel, context switching between tasks.

### Async programming 
- Asynchronous programming is basically managing tasks that might take some time to complete, such as I/O operations, without blocking the execution of the rest of the code. 

- The runtime environment handles context switching between tasks to ensure efficient execution.

### How does JS being a single threaded language does parallel jobs?

- By using async functions
- Basic functions are sync in nature but there are some async functions inbuilt in js such as
    - `setTimeout(() ⇒ {does something}, time_in_ms);`
    - `fs.readfile()`
    - `fetch(callback)`

### Async architecture of js

- **callstack** → The call stack is a data structure that keeps track of function calls in your code. When a function is called, a new frame is pushed onto the stack. When a function completes, its frame is popped from the stack. This is how JavaScript manages the flow of execution.
- **webapis →** Web APIs are functionalities provided by the browser or the environment in which JavaScript is running. Here most of the async operations are put until they complete.
- **callback queue** → When asynchronous operations complete, their corresponding callbacks are pushed into the callback queue. For example, when a network request or a timer completes, its callback is placed in the callback queue to be executed later.
- **eventloop** → The event loop is a continuous process that constantly checks the call stack and the callback queue. If the call stack is empty, the event loop takes the first callback from the queue and pushes it onto the stack, allowing it to be executed. This mechanism enables JavaScript to handle asynchronous tasks without blocking the main thread.

Let’s understand it with an example:

```jsx
console.log("a");

setTimeout(() => {
	console.log("");
}, 5000);

let a = 0;

for (looping till 10) {
	console.log(i);
}
```

Explanation: 

1. console.log → callstack → pop
2. setTimeout → webapis (timer running) → completed → callback queue (waiting for its turn to be pushed back into the callstack by eventloop)
3. while timer let a = 0 → callstack → pop
4. Loop → callstack → pop → thread is idle now
5. setTimeout’s callback → callstack (by eventloop) → popped

---

### How can we make our own async code?

1. By wrapping up the inbuilt js async function inside our own created function
2. By using promises 