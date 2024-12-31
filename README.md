# React setInterval Memory Leak
This example demonstrates a common error in React components: using `setInterval` inside `useEffect` without a cleanup function. This leads to memory leaks and unexpected behavior.

## Bug Description
The `MyComponent` uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts. This results in the interval continuing to run even after the component is no longer rendered, leading to memory leaks and potentially incorrect behavior.

## Solution
The solution involves using a cleanup function within the `useEffect` hook to clear the interval before the component unmounts.