# Unhandled Error in Asynchronous Node.js Server

This repository demonstrates a common error in Node.js applications: neglecting to handle errors that occur within asynchronous operations.  The server simulates an asynchronous task that can randomly succeed or fail.  The failure case is not handled properly, causing the error to be silently swallowed.

## Bug

The `bug.js` file contains the buggy server code.  The server responds with a 500 error when the simulated asynchronous operation fails. However, there is no error handling, leading to a lack of logging or any other mechanism to alert the developer about the failure.

## Solution

The `bugSolution.js` file demonstrates the correct way to handle errors.  It utilizes a `try...catch` block to catch potential errors and logs them to the console.  This ensures that the developer is notified of failures.

This example highlights the importance of comprehensive error handling in asynchronous Node.js applications to ensure stability and maintainability.