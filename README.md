# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The provided code uses `useEffect` without proper dependency array management, leading to an infinite render loop.  The solution demonstrates how to correctly use dependencies to fix this issue.

## Bug
The `useEffect` hook in the `bug.js` file is called after every render, resulting in an infinite loop.  Observe the console log in a browser.  This is because the dependency array is missing. This unnecessary re-renders greatly impacts performance.

## Solution
The `bugSolution.js` file provides the corrected code.  Adding `[count]` as a dependency array ensures the effect only runs when the `count` value changes, thus resolving the infinite loop.