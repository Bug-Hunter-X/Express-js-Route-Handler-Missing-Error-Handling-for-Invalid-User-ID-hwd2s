# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user inputs.  Specifically, this example shows a route that retrieves a user by ID, but fails to handle cases where the ID is not a valid integer.

## Bug

The `bug.js` file contains the faulty code.  The route handler attempts to parse the user ID as an integer using `parseInt()`, but doesn't check if the result is a valid integer or handle potential errors if parsing fails. This can lead to unexpected behavior or crashes.

## Solution

The `bugSolution.js` file provides a corrected version of the route handler.  It includes explicit error handling to gracefully manage cases where the user ID is invalid or the user is not found.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `npm install express` to install the required dependencies.
4. Run `node bug.js` and then send a request to `/users/abc` (invalid user ID). Observe the error.
5. Run `node bugSolution.js` and then send a request to `/users/abc`. Observe the improved error handling.