# React useEffect Dependency Array Bug

This repository demonstrates a common error in React's `useEffect` hook: improperly managing the dependency array, leading to infinite re-renders. 

The `bug.js` file contains the faulty code.  The `bugSolution.js` provides the corrected version.

## The Problem

The original code causes an infinite loop because the `useEffect` hook is called every time the component renders. This is because the `count` variable is used inside the effect, but it is not listed in the dependency array. This leads to the effect firing repeatedly, causing a cycle of renders and updates.

## The Solution

The solution includes `count` in the dependency array. This ensures that the effect only runs when `count` changes, thus breaking the infinite render loop.