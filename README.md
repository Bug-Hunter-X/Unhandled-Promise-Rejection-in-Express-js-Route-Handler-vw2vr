# Unhandled Promise Rejection in Express.js

This repository demonstrates a common error in Express.js applications: unhandled promise rejections.  The `bug.js` file contains code that performs an asynchronous operation but lacks proper error handling. This can lead to unexpected application crashes or silent failures.

The `bugSolution.js` file provides a corrected version with comprehensive error handling using a `try...catch` block to manage asynchronous operations effectively and a central error handler for uncaught exceptions.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory in your terminal.
3. Run `node bug.js`. Observe the lack of explicit error handling, and the process might exit unexpectedly.
4. Run `node bugSolution.js`. Observe the improved error handling, preventing crashes and providing informative error messages.

## Solution

The solution involves adding a `catch` block to the promise chain to handle potential errors gracefully. This prevents unhandled promise rejections and allows for better error management and logging.