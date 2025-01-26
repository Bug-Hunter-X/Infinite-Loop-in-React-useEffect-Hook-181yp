# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include state variables in the dependency array, leading to an infinite render loop.

## Bug Description
The `MyComponent` component uses `useState` to manage a count.  The `useEffect` hook logs the current count.  However, `count` is missing from the dependency array. This causes the effect to run after every render, triggering a state update, resulting in an infinite loop.

## Bug Solution
The solution involves adding `count` to the dependency array. This ensures the effect only runs when the count changes.

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs in your browser's developer tools. You'll see the infinite loop.
5. Refer to `bugSolution.js` for the corrected code.
