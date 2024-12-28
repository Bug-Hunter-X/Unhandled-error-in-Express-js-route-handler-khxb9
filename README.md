# Unhandled error in Express.js route handler

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without checking for errors. If the parameter is not a valid integer, it will cause a runtime error.

The `bug.js` file shows the problematic code. The `bugSolution.js` file provides a solution that includes comprehensive error handling.

## How to reproduce the bug

1. Clone this repository.
2. Run `npm install` to install the required packages.
3. Run `node bug.js`.
4. Send a GET request to `/users/abc` (or any non-numeric ID).
5. Observe the error message in your console.

## Solution

The solution involves adding error handling to gracefully manage cases where the `id` parameter is not a valid integer. The `bugSolution.js` file provides the corrected code.