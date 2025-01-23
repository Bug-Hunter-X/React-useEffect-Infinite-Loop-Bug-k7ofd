# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.  The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

## Problem

The `useEffect` hook in `bug.js` is intended to log the current count to the console.  However, because the `count` variable is not included in the dependency array, the effect runs after every render, regardless of whether `count` has actually changed.  This creates an infinite render loop. 

## Solution

The `bugSolution.js` file corrects the problem by including `count` in the dependency array.  Now, the effect only runs when `count` changes, preventing the infinite loop.