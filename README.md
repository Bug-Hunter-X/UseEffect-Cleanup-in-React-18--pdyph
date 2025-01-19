# React 18 useEffect Cleanup Bug

This repository demonstrates a common error in React 18 and above related to the `useEffect` hook.  Forgetting to include a cleanup function within the `useEffect` hook can cause memory leaks and unexpected behavior.  This example showcases the problem and provides a solution.

## The Bug

The `bug.js` file contains a component that uses `setInterval` within a `useEffect` hook but lacks the necessary cleanup function to stop the interval when the component unmounts. This can lead to memory issues as the interval continues even after the component is removed.

## The Solution

The `bugSolution.js` file presents the corrected component, which includes a return function in the `useEffect` hook that calls `clearInterval` to properly clean up the interval when the component is unmounted.  This ensures efficient resource management and avoids memory leaks.
