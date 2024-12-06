# Next.js 15 Unhandled Runtime Error in Route Navigation

This repository demonstrates a bug in Next.js 15 where a runtime error thrown within a page component isn't gracefully handled during client-side navigation.  This leads to a poor user experience.

## Bug Description

The `pages/about.js` intentionally throws an error.  Navigating to `/about` from `/` causes a crash without proper error handling on the client-side. The default Next.js error page is shown, but a more refined error handling mechanism is desired.

## Reproduction Steps

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Navigate to `http://localhost:3000`. 
5. Click the link to the '/about' page.
6. Observe the error page.

## Solution

A more robust solution would involve implementing centralized error handling in the Next.js application using features like error boundaries.  This would allow for a more user-friendly approach to handling these runtime exceptions during navigation or other application actions.
