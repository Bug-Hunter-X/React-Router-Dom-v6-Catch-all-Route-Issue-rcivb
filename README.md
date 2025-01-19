# React Router Dom v6 Catch-all Route Issue

This repository demonstrates an unexpected behavior in React Router Dom v6 when using a catch-all route ('/*') alongside other more specific routes. The catch-all route seems to always match, even when a more specific route should match first.

## Bug Description

In the example application, we have three routes:

- '/' : Home page
- '/about' : About page
- '/*' : 404 Not Found page (catch-all)

The expectation is that when accessing '/about', the About component should be displayed. However, the 404 component is rendered instead because the catch all route always matches.

## Steps to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Navigate to '/about'. The 404 page will be displayed instead of the About page.

## Solution

The issue is resolved by placing the catch-all route last in the Routes.  See AppSolution.js for the solution.