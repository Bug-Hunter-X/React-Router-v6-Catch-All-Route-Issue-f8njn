# React Router v6 Catch-All Route Bug

This repository demonstrates a bug in React Router v6 related to the catch-all route ("/*"). The catch-all route unexpectedly overrides other defined routes, even when a matching route exists. This behavior is inconsistent and can lead to unexpected page rendering.

## Reproduction Steps:

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to `/` or `/about`.  The catch-all route renders instead of the expected route.

## Solution:

The solution involves reordering routes within the `<Routes>` component.  Place the catch-all route last. This ensures the other routes are checked first, resulting in the correct rendering.