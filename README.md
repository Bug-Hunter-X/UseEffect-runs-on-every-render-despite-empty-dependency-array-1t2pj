# React useEffect Bug: Unexpected Re-renders

This repository demonstrates a common yet subtle issue with the React `useEffect` hook.  The effect runs on every render, even though an empty dependency array is specified, which should restrict it to only running once after the initial render.

## Bug Description:

The `useEffect` hook is intended to perform side effects after a component renders. When an empty dependency array `[]` is provided, it's expected to run only once, on mount. However, the effect in this example triggers multiple times, resulting in unnecessary console logs.

## Solution:

The solution involves verifying the state and props of the component to make sure that there is nothing that's causing a re-render. If not then there's something external to the component causing the effect to fire.