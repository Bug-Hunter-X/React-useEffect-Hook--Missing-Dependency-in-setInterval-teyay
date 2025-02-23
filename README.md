# React useEffect Hook: Missing Dependency in setInterval

This example demonstrates a common mistake when using the `useEffect` hook in React: forgetting to include necessary dependencies in the dependency array. This can lead to unexpected behavior, such as infinite loops or incorrect updates.

## The Bug
The `bug.js` file contains a component that uses `setInterval` to update a counter every second. However, the dependency array for `useEffect` is empty (`[]`). This means that the effect runs only once after the component mounts and the `setInterval` is never cleared.

## The Solution
The `bugSolution.js` file shows the corrected version.  The `count` variable is added to the dependency array.  Now the effect will run again whenever the value of `count` changes and the previous interval is cleared, preventing memory leaks and other issues.