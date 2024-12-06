# React 19 useEffect setInterval Memory Leak
This repository demonstrates a common error in React 19 applications involving the `useEffect` hook and the `setInterval` function.  Forgetting to include a cleanup function within `useEffect` when using `setInterval` can lead to memory leaks and unexpected behavior.  This example illustrates the problem and provides a solution.

## Problem
The `bug.js` file showcases an incorrect implementation. The `setInterval` function is used to update a counter every second. However, the component fails to clear the interval when it unmounts, leading to memory leaks.

## Solution
The `bugSolution.js` file demonstrates the correct implementation.  The `useEffect` hook returns a cleanup function that uses `clearInterval` to stop the interval when the component is unmounted. This prevents memory leaks and ensures the application runs smoothly.  Consult React's documentation on useEffect for detailed information on the proper usage of the cleanup function.