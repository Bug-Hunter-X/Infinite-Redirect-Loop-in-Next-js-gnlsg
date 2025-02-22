# Infinite Redirect Loop in Next.js

This repository demonstrates a common error in Next.js applications: an infinite redirect loop.  The error occurs when using the `useRouter` hook to navigate to the current route, creating a continuous redirect cycle.

## Problem

The `bug.js` file contains a component that uses `useRouter.push('/')` to navigate to the home route. If the component is already on the home route ('/'), this causes an infinite redirect, leading to a browser crash or unresponsive application.

## Solution

The `bugSolution.js` file demonstrates how to avoid this issue using the `router.asPath` property to check the current route. This prevents unnecessary redirects.