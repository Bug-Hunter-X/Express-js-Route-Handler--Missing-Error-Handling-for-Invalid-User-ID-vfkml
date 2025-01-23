# Express.js Route Handler: Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: insufficient error handling for invalid input.  Specifically, the provided code attempts to access a user based on an ID passed in the route parameter.  However, it lacks proper validation and error handling for cases where the provided ID is not a number, leading to potential crashes or unexpected results.

The `bug.js` file showcases the erroneous code, while `bugSolution.js` presents a corrected version with improved error handling.

## Bug
The primary issue lies in the lack of input validation for the `userId`.  If a non-numeric value is passed as an ID, `parseInt(userId)` will return `NaN`, leading to a failure in finding the user and potentially causing an error.