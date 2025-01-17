# Next.js 15 Environment Variable Access Error

This repository demonstrates a common error in Next.js 15 applications when attempting to access environment variables directly in client-side code.  The `process.env` object is only populated on the server-side.

## Problem

The `about.js` file attempts to access `process.env.MY_VARIABLE`.  This will result in a runtime error in the browser because `process.env` is undefined in the client environment.

## Solution

To solve this issue, environment variables should be accessed on the server-side and passed to the client-side components as props.  This example shows how to achieve that by adding a simple API route.

## How to Reproduce

1. Clone the repository.
2. Install dependencies using `npm install`.
3. Start the development server using `npm run dev`.
4. Navigate to the `/about` page.
5. Observe the error in the browser console.

## How to Fix

Refer to the updated `about.js` and `pages/api/env.js` files for a solution using an API route.