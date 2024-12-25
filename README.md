# Unhandled Promise Rejection in Express.js

This repository demonstrates a common error in Express.js applications: unhandled promise rejections.  When asynchronous operations within request handlers fail without proper error handling, the server can crash.

## Bug

The `bug.js` file contains an Express.js server with an asynchronous operation (`someAsyncOperation`). If this operation fails, the error is not caught, leading to a crash.

## Solution

The `bugSolution.js` file provides the corrected code. It includes a `.catch()` block to handle potential errors, preventing the server from crashing.  Error handling is crucial for building robust and reliable applications.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install the required dependencies.
3. Run `node bug.js` to start the server with the bug.  Observe crashes.
4. Run `node bugSolution.js` to start the server with the solution.  Observe the error is gracefully handled.