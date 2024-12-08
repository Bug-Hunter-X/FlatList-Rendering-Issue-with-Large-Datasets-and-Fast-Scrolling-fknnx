# React Native FlatList Rendering Bug

This repository demonstrates a common bug encountered when using the FlatList component in React Native with large datasets and rapid scrolling. The bug manifests as incorrect rendering, displaying blank spaces or the wrong data in the list.

The issue is exacerbated when the data is dynamic, meaning it's updated frequently. The provided code snippets illustrate the problem and its solution.

## Problem
The `FlatListBug.js` file shows a basic implementation of FlatList that renders a large number of items. When scrolling quickly, inconsistent rendering occurs.

## Solution
The `FlatListBugSolution.js` file demonstrates a solution which uses the `getItemLayout` prop to significantly improve the rendering performance of the FlatList by providing the dimensions of each item in advance. This enables the FlatList to render items more efficiently, even with fast scrolling and large datasets. 

## How to Reproduce
1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run the app on an Android or iOS emulator or device using `npx react-native run-android` or `npx react-native run-ios`.
4. Scroll quickly through the list to observe the rendering errors in `FlatListBug.js`. Compare with the corrected behaviour of `FlatListBugSolution.js`.