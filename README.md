# React Native AsyncStorage: Retrieving Data Before Storage Completion

This repository demonstrates a common bug in React Native applications when using AsyncStorage to store and retrieve data. The issue arises when attempting to retrieve data before the storage operation has fully completed, leading to unexpected null or undefined values.

## Bug Description
The asynchronous nature of AsyncStorage operations can cause problems if data retrieval is attempted before storage is finished. This commonly happens when promises or callbacks are not handled correctly. The bug.js file showcases this issue.  The bugSolution.js file demonstrates the correct way to handle this situation.

## How to reproduce
1. Clone the repository.
2. Run `npm install`.
3. Run the application (you'll need a React Native environment set up).
4. Observe the console output, where you'll see the problem and its fix.

## Solution
The solution involves ensuring that data retrieval happens only after the storage operation is successfully completed using `.then()` or `async/await` (shown in bugSolution.js).