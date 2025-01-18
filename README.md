# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, the route `/users/:id` attempts to parse the `id` parameter as an integer without handling potential errors if the `id` is not a number.

## Bug

The `bug.js` file contains the erroneous code.  It fetches a user by ID but fails to handle cases where the ID is not a valid integer. This can lead to crashes or unexpected behavior.

## Solution

The `bugSolution.js` file provides a corrected version of the code. It includes comprehensive error handling using `isNaN()` to check if the ID is a valid number.  If not, it returns an appropriate error response.

## How to run

1. Clone this repository.
2. Navigate to the directory.
3. Run `node bug.js` (to see the error) and then `node bugSolution.js` (to see the corrected version)