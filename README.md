# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The issue arises from omitting the dependency array in `useEffect`, leading to an infinite render loop.

## Bug Description

The `MyComponent` component uses `useEffect` to log the current `count` value to the console after each render. However, because the dependency array is missing, the effect runs after every state update, causing a continuous cycle of rendering and logging.

## Solution

The solution involves specifying the `count` variable within the dependency array. This ensures that the effect only runs when the `count` value changes.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `npm start` to start the development server.
4. Observe the continuous logging to the console and the unresponsive UI.
5. Examine the `bugSolution.js` file to see the corrected code.