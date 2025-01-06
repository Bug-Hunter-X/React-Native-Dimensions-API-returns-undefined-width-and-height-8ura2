# React Native Dimensions API Undefined Width and Height Bug

This repository demonstrates a common bug in React Native where the `Dimensions` API returns undefined `width` and `height` properties, leading to crashes or unexpected behavior.  The solution involves using the `onLayout` event or `useEffect` hook with a cleanup function to ensure the dimensions are available before using them. 

## Bug Description
The `Dimensions` API in React Native, when used to get screen dimensions, sometimes returns `undefined` values for `width` and `height`, particularly during app startup or screen rotation. This causes unexpected behavior or app crashes if components attempt to access the dimensions before they are available.  This example shows this issue and a suggested solution.

## Solution
The provided solution employs the `onLayout` event to ensure the dimensions are available before rendering the component.  This prevents crashes and ensures a consistent user experience.