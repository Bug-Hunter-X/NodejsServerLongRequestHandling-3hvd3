# Node.js Server Hangs on Long Requests

This repository demonstrates a common issue in Node.js servers: hanging on long-running requests.  The provided code creates a simple HTTP server that simulates a long-running task (a 5-second delay).  Without proper asynchronous handling, this blocks the event loop, preventing the server from responding to other requests.

The `server.js` file contains the buggy code. The `serverSolution.js` file showcases a solution using asynchronous operations to prevent blocking and maintain server responsiveness.

## How to reproduce the bug:

1. Clone the repository.
2. Run `node server.js`.
3. Send multiple requests to `http://localhost:3000`.
4. Observe that the server becomes unresponsive after the first request.

## How the solution works:

The solution uses asynchronous programming techniques to handle long-running tasks without blocking the event loop. This ensures that the server remains responsive even under heavy load. This is implemented through more robust methods to prevent the server from hanging during long-running processes.