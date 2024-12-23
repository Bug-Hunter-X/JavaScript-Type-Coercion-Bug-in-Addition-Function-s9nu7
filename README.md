# JavaScript Type Coercion Bug

This repository demonstrates a subtle bug in a JavaScript addition function related to type coercion. The function `foo` returns `null` if either input is `null` or `0`. This behavior is unexpected when one of the inputs is `0`, as it should mathematically add zero to the other number.

## Bug Description
The function `foo` incorrectly handles the case where either `a` or `b` is `0`. Instead of treating `0` as a number and performing the addition, it treats `0` as loosely equal to `null`, leading to an incorrect `null` result.

## How to Reproduce
1. Clone this repository.
2. Open `bug.js`.
3. Run the code using a JavaScript runtime (Node.js, browser console, etc.).
4. Observe the unexpected output for cases where one of the inputs is 0.

## Solution
The solution involves using strict equality (`===`) to explicitly check for `null` values only, avoiding type coercion that might incorrectly treat `0` as equivalent to `null`.