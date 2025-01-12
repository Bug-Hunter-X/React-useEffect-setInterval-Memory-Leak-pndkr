# React useEffect setInterval Memory Leak

This repository demonstrates a common error in React applications involving the use of `setInterval` within the `useEffect` hook.  Failure to properly clear the interval when the component unmounts leads to a memory leak.

The `bug.js` file contains the buggy code, and `bugSolution.js` shows the corrected version.

## Problem

The `setInterval` function continues to run even after the component is unmounted. This causes the interval to continue unnecessarily consuming resources, creating a memory leak.

## Solution

The solution involves using a cleanup function within the `useEffect` hook to clear the interval using `clearInterval` before the component is unmounted.  This ensures that the interval is stopped, preventing the memory leak.