# MongoDB Aggregation Pipeline Bug: Incorrect $inc operator usage

This repository demonstrates a common error when using the `$inc` operator within the `$project` stage of a MongoDB aggregation pipeline. The `$inc` operator is designed to increment a numeric field by a specified value. However, providing it with an array leads to an error.

## Bug Description
The `$inc` operator is incorrectly used with an array as the value in the `$project` stage.  This leads to an error because `$inc` expects a numeric value or a field path.

## Solution
The solution involves using the `$add` operator to properly increment the `count` field instead of `$inc`.