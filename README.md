# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.

## Description
The `MyComponent` component uses `useEffect` to log the current `count` state to the console.  However, the dependency array `[count]` is incorrectly missing, causing the effect to run after every render, leading to an infinite loop.

## Solution
The solution involves correctly specifying the dependency array. If the effect depends on the `count` variable, then it must be included in the dependency array.