# MongoDB $inc Operator Error
This repository demonstrates a common error encountered when using the `$inc` operator in MongoDB update queries and provides a solution.

## Problem
The `$inc` operator is used to increment a numeric field in MongoDB. However, if the field doesn't exist or is not a number, it can throw an error.

## Solution
To handle cases where the field might not exist, use the `$setOnInsert` operator in conjunction with `$inc`. This ensures that the field is created with a default value (1 in this example) if it doesn't exist, and then incremented.

## Files
* `bug.js`: Demonstrates the incorrect usage of the `$inc` operator.
* `bugSolution.js`: Shows the corrected usage of `$inc` with `$setOnInsert`.