# React useEffect Hook Unexpected Behavior

This repository demonstrates a common issue with the React `useEffect` hook when using an empty dependency array.  The effect runs only once on mount, which can lead to unexpected behavior if the component's state changes.  The solution demonstrates a correct usage of the dependency array. 

## Problem
The `bug.js` file shows an example where the `useEffect` hook is used with an empty dependency array. While this will correctly log 'Mounted!' once, it won't update when `count` changes.  This causes the effect to run only once on mount and not when `count` updates. 

## Solution
The `bugSolution.js` file corrects this issue by including `count` in the dependency array.  Now, the effect will re-run whenever `count` changes.