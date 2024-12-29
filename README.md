# Express.js: Missing Status Code in Successful API Response

This repository demonstrates a common, yet subtle, error in Express.js applications: omitting the status code in successful API responses.

## Bug Description
The `bug.js` file contains an Express.js route handler that fetches user details.  If a user is not found, it correctly returns a 404 status code. However, if a user *is* found, it sends the user data without specifying a status code. This inconsistency can lead to issues in consuming applications.

## Solution
The `bugSolution.js` file demonstrates the solution: explicitly setting the status code to 200 (OK) when returning the user data. This ensures consistent and predictable API responses, improving maintainability and reducing potential client-side errors.