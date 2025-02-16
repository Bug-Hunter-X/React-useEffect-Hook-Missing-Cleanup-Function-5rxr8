## React useEffect Hook Missing Cleanup Function
This repository demonstrates a common error in React applications: forgetting to include a cleanup function in the `useEffect` hook.  This can lead to memory leaks or unexpected behavior when components unmount.

The `bug.js` file shows the problematic code. The `bugSolution.js` file demonstrates the correct usage of useEffect with a cleanup function.

**Problem:** The `useEffect` hook in `bug.js` logs a message when the component mounts. However, it lacks a cleanup function to perform any necessary actions (like clearing intervals, unsubscribing from events, etc.) when the component unmounts. This can result in memory leaks if the effect creates resources that are not properly released.

**Solution:** The `bugSolution.js` file shows how to add a cleanup function to the `useEffect` hook using the return statement.  This function is executed when the component unmounts, allowing for proper cleanup.
