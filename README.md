# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler can cause the server to become unresponsive. The example uses a `setTimeout` function to simulate this behavior.  The solution demonstrates how to use asynchronous programming to prevent this problem.

## Bug
The `bug.js` file contains a Node.js server that simulates an unresponsive server by introducing a 5-second delay within the request handler. This delay blocks the event loop, preventing the server from responding to subsequent requests during that time.

## Solution
The `bugSolution.js` file shows the correct implementation, using asynchronous programming to avoid blocking the event loop, enabling the server to handle multiple concurrent requests.