# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js: server unresponsiveness caused by long-running synchronous operations within the request handler.  The example uses a simple HTTP server with a computationally expensive loop that blocks the event loop, preventing the server from handling further requests.

The `server.js` file shows the problematic code. The `serverSolution.js` file provides a solution using asynchronous operations or worker threads to avoid blocking the event loop.

## How to Reproduce
1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `node server.js`.
4. Try to access the server using a browser or `curl`.  You will observe that the server becomes unresponsive after the first request.
5. To see the corrected behavior, run `node serverSolution.js`