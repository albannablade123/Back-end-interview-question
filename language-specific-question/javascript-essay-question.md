

## What is the difference between Node.js and JavaScript?
JavaScript is a scripting language whereas Node.js is an engine that provides the runtime environment to run JavaScript code.

## Is Node.js single-threaded?

Yes, Node.js is single-threaded by default. However, it utilizes **event-driven** architecture and non-blocking I/O operations to handle multiple concurrent requests efficiently, enabling scalability and high performance in applications

## What is the difference between Synchronous and Asynchronous functions? 

### Synchronous 
- Block execution until task completes
- Executes task sequentially
- Returns the result immidiately after completion

### Asynchronous
- Does not block the execution; allows other task to proceed
- Initiates tasks and proceeds with other operations while waiting for completion
- Return a promise, callback or event handling to handle result

## What is a module:
- Considered as a block of coded that provide a simple or complex functionality that can communicate with external application

## What is npm and its advantages
Default package manager for Node.js. Allows develoepr to discover share and reuse code packages

## What is middle wear
A function that works between the request and response code.

## What is control flow in Node.js
Refers to the sequence which statements are executed.
. It manages the order of execution, handling asynchronous operations, callbacks and error handling.

## What is meant y event loop in Node.js
A mechanism that allows Node.js to handle multiple asynchronous tasks concurrently. Continously listen for events and executes callback function.

## State the order in which control flow statements gets executed:
The order in which the statements are executed is as follows:

- Execution and queue handling
- Collection of data and storing it
- Handling concurrency
- Executing the next lines of code

## What is REPL in Nodejs.
REPL stands for Read, Evaluate, Print and Loop. Similiar to a shell.

## What are promises 
- A promise is basically an advancement of callbacks in NodeJS. In other words, a promise is a JavaScript object which is used to handle all the asynchronous data operations. 
- While developing an application you may encounter that you are using a lot of nested callback functions which causes a problem of callback hell. Promises solve this problem of callback hell.

## What is buffer in Node.js?
The Buffer class in Node.js is used to perform operations on raw binary data. Generally, Buffer refers to the particular memory location in memory.

## Wha are streams in Node.js
- type of data-handling method and are used to read or write input into output sequentially.
- Streams are used to handle reading/writing files or exchanging information in an effecient way.

## Explain the use of timers module in Nodejs
- Timer module contain various function that execute a block of function after a set period of time.

## What is a web socker
- Web socket is a protocol that provides full-duplex communication i.e allows communication in both direction simultaneously. It is a modern web technology in where there exist a continous connection between user and server. Unlike HTTP connection, webSocket is continously open. 

## What is the main difference between setImmidiate() and process.nextTick()

The SetImmidiate is designed to execute the callback function on the next iteration of the event loop. Its used to break up long operation and allow I/O events to be processed

nextTick() adds the callback to the next tick queue which is processed immidiately. Used to execute code asynchronously. 

## What is a body parser in Node.JS
Body-parser is the Node.js body-parsing middleware. It is responsible for parsing the incoming request bodies in a middleware before you handle it. It is an NPM module that processes data sent in HTTP requests.

## What is CORS in Node.js
CORS, or Cross-Origin Resource Sharing, is a mechanism that allows web applications to make requests to a server hosted on a different domain than the one from which the application was loaded. This is essential for enabling cross-origin requests in web applications, which are otherwise restricted by the same-origin policy in web browsers.
