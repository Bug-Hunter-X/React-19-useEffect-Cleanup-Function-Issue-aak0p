# React 19 useEffect Cleanup Function Issue

This repository demonstrates a common issue encountered when using the `useEffect` hook in React 19. The problem arises from an improper understanding of the dependency array and how it affects the cleanup function.

## The Problem
The `useEffect` hook in the provided `bug.js` file has an incomplete dependency array.  This causes the effect to run repeatedly, leading to an infinite loop of console logs. The cleanup function, intended to run before the next effect, is not called as expected.

## The Solution
The solution in `bugSolution.js` corrects the dependency array in `useEffect`. By correctly specifying `count` in the array, we ensure that the effect only runs when the value of `count` changes.  This addresses the infinite loop and allows the cleanup function to behave as expected. 

## How to reproduce:
1. Clone the repo
2. Run `npm install`
3. Run `npm start`
4. Observe the console logs in `bug.js`. Notice how the cleanup function doesn't run appropriately.
5. Compare this to the corrected code in `bugSolution.js` which provides the intended behavior. 
