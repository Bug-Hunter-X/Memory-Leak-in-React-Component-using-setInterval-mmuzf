# React setInterval Memory Leak

This example demonstrates a common mistake when using `setInterval` within a React component's `useEffect` hook.  Without proper cleanup, the interval continues to run even after the component unmounts, leading to memory leaks.

## Bug

The `bug.js` file contains a React component that uses `setInterval` to update a count every second. However, it lacks the necessary cleanup function to stop the interval when the component unmounts.

## Solution

The `bugSolution.js` file provides a corrected version.  It uses the return value of `useEffect` to specify a cleanup function that calls `clearInterval` to stop the interval before the component is unmounted, preventing the memory leak.
