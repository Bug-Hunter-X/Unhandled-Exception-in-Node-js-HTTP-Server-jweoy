# Unhandled Exception in Node.js HTTP Server

This repository demonstrates an example of an unhandled exception in a Node.js HTTP server and how to handle it gracefully.

## Bug Description
The server is missing error handling for unexpected events during request processing. This can lead to the server crashing and becoming unavailable.

## Bug Reproduction
1. Clone this repository.
2. Run `node server.js`.
3. The server will start listening on port 8080.
4. Try to access the server; it'll work fine.
5. Modify server.js to introduce an error (e.g.,  accessing a non-existent property) within the requestListener function. This will lead to an unhandled exception, causing the server to terminate abnormally.

## Solution
The solution involves using a `try...catch` block to handle potential errors during request processing and gracefully respond to the client with an error message. This prevents the server from crashing.