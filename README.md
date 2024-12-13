# React useEffect Infinite Loop Bug
This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug causes an infinite loop of re-renders due to improper usage of the dependency array.

## Bug Description
The `useEffect` hook is used to fetch data from an API and update the component's state. However, the dependency array is empty (`[]`), causing the effect to run on every render.  This leads to continuous API calls and an infinite loop.

## Solution
The solution involves correctly specifying the dependency array. If the effect depends on external data, add the data fetching logic to the dependency array or use `useCallback` and `useMemo` to prevent unnecessary recalculations.

## How to reproduce
1. Clone this repository.
2. Run `npm install`
3. Run `npm start`
4. Observe the infinite loop in the browser's developer console.