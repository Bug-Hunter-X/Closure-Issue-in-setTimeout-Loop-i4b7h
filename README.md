# Closure Issue in setTimeout Loop

This repository demonstrates a common closure-related bug in JavaScript when using `setTimeout` within a loop.  The issue arises because the `setTimeout` callback function doesn't capture the value of `i` at each iteration; instead, it captures the reference to `i`. By the time `setTimeout` finally executes, the loop has already completed, and `i` is 10.

The `bug.js` file contains the buggy code, and `bugSolution.js` provides a corrected version.

## How to Reproduce
1. Clone this repository.
2. Open `bug.js` and `bugSolution.js` in your preferred JavaScript environment (e.g., browser's console, Node.js).
3. Execute `bug.js`. Observe that all alerts display '10'.
4. Execute `bugSolution.js`. Observe that each alert displays the correct value of `i` at the time of each iteration.