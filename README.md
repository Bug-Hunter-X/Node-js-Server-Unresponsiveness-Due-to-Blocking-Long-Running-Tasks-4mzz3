# Node.js Server Unresponsiveness Due to Blocking Long-Running Tasks

This repository demonstrates a common Node.js issue: server unresponsiveness caused by long-running tasks that block the event loop.  The `bug.js` file showcases the problem, while `bugSolution.js` provides a solution using asynchronous operations.

## Problem

Node.js is single-threaded.  When a long-running operation blocks the event loop, the server becomes unresponsive to new requests. This can significantly impact the application's performance and user experience.

## Solution

The solution involves using asynchronous operations (like promises or async/await) to avoid blocking the event loop.  This allows the server to continue processing other requests while the long-running task executes in the background.