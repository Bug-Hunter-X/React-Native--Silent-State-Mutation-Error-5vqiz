# React Native Silent State Mutation Bug

This repository demonstrates a common, yet subtle, bug in React Native applications: directly mutating state within a functional component.  This can lead to unexpected behavior and UI inconsistencies because React's internal state management system won't detect the change.

## The Bug
The `bug.js` file shows a functional component with a state variable that's being directly modified.  This violates React's state update mechanism and results in the UI not reflecting the changes.

## The Solution
The `bugSolution.js` file corrects this by using the `useState` hook correctly.  This ensures that React manages state updates, triggering re-renders and correctly updating the UI.

## How to Reproduce
1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install`.
4. Run `npx react-native run-android` or `npx react-native run-ios`.
5. Observe the UI behavior in both `bug.js` and `bugSolution.js` to see the difference.