# React useEffect Cleanup Function Not Called

This repository demonstrates a common issue in React where the cleanup function in `useEffect` is not called as expected, leading to potential memory leaks.

## Problem

The provided `MyComponent` uses `useEffect` to log the current count and performs a cleanup.  However, the cleanup function might not be called under certain circumstances, such as rapid component re-renders.  The dependency array `[count]` is crucial for proper behavior. Without it, the effect will run after every render which is not the desired behavior.