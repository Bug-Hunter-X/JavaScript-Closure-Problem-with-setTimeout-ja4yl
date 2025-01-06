# JavaScript Closure Problem with setTimeout

This repository demonstrates a common issue in JavaScript related to closures and the `setTimeout` function.

The problem arises when using `setTimeout` within a loop. The closure created by the `setTimeout` callback does not capture the value of `i` at the time the callback is created, but rather captures a reference to the variable `i`. As a result, by the time the `setTimeout` callbacks finally execute, the loop has already completed, and `i` will have its final value (10 in this case). 

The solution involves creating a new scope for `i` using an immediately invoked function expression (IIFE) or using `let` to create a block scope variable.

## How to run

1. Clone this repository.
2. Open `bug.js` to see the problematic code.
3. Open `bugSolution.js` to see the corrected code. 
4. Open your browser's developer console and run the code in each of the files to observe the different behaviors.