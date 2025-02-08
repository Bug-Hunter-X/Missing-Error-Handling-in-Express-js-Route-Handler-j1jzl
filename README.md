# Express.js Route Handler Bug: Missing Error Handling

This repository demonstrates a common bug in Express.js route handlers:  lack of error handling for invalid input.  The provided code attempts to find a user based on their ID, but it doesn't handle cases where the ID is not a valid number, resulting in potential errors.

The `bug.js` file contains the buggy code, and `bugSolution.js` provides a corrected version with appropriate error handling.

## Bug:

The main issue is the absence of input validation. The code directly attempts to parse the user ID as an integer without checking if it's a valid number. If a non-numeric ID is provided, `parseInt(userId)` will return `NaN`, leading to an incorrect search and the potential for application crashes or unexpected behavior.