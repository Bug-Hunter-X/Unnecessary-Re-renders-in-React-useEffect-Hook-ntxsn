# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common issue in React applications where the `useEffect` hook causes unnecessary re-renders.  The provided example shows a simple counter component where the `useEffect` hook logs a message to the console after every render. While this is not inherently wrong for small examples, in larger applications, it can cause performance issues.

## Problem

The `useEffect` hook in the original code lacks an appropriate dependency array, causing it to execute after every render, regardless of whether the state has changed.

## Solution

The improved code includes `[count]` as the dependency array. This ensures the `useEffect` hook only runs when the `count` state variable changes, significantly improving performance.

## How to Run

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.  Observe the console output.  The fixed version shows dramatically fewer console messages.