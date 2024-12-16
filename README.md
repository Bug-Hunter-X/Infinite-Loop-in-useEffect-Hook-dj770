# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook causing an infinite loop.  The problem arises from omitting necessary dependencies in the `useEffect` dependency array, leading to the effect running on every render, creating a continuous cycle.

## Bug Description
The `useEffect` hook in the provided component is missing `count` in its dependency array. This causes the effect to run infinitely because the `console.log` statement within the effect triggers a re-render and leads to the effect running continuously. This renders the component unstable. 

## Solution
By adding `count` to the dependency array, the effect will now only run when the `count` variable changes, resolving the infinite loop.