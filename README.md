# React Router Unexpected Route Matching
This repository demonstrates a common issue encountered when using `react-router-dom` and how to resolve it.

## Problem
The `path="/*"` route in `react-router-dom` is often used for a 404 Not Found component.  However, it can cause unexpected behavior if placed after other routes, as it will match any path, overriding more specific routes.

## Solution
The `path="/*"` route should always be placed last within the `Routes` component to ensure that it only matches paths that haven't already been matched by other more specific routes.

## How to reproduce
Clone this repository, run `npm install`, and then run `npm start`. Navigate to different paths like `/`, `/about`. Observe the issue where the 404 page always shows up.