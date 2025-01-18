# Stale Closure in useEffect with setInterval

This repository demonstrates a common error in React when using the `useEffect` hook with `setInterval`.  The problem arises from stale closures, where the callback function within `setInterval` retains a reference to the initial state value, leading to unexpected behavior.

The `bug.js` file contains the erroneous code. The `bugSolution.js` file shows the corrected implementation.

## Bug
The incorrect code uses `setInterval` inside `useEffect` to update a state variable every second. However, the callback function within `setInterval` uses the initial value of the state variable, leading to the counter not updating correctly. 

## Solution
The solution uses functional updates to ensure the `setCount` function always uses the latest state value.