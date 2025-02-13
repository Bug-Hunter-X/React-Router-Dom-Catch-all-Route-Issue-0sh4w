# React Router Dom Catch-all Route Issue

This repository demonstrates an unexpected behavior with the catch-all route (`/*`) in React Router Dom v6.  The catch-all route is always triggered, even when a valid route exists. This issue occurs when the catch-all route is placed after other routes that have more specific paths. 

## How to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Notice that even when navigating to `/` or `/about`, the `NotFound` component is always rendered.

## Solution
The solution involves reordering the routes in the `Routes` component. The catch-all route must always be placed last.  See `AppSolution.js` for the corrected code.