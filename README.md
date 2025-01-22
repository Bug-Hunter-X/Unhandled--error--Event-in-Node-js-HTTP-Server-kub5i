# Unhandled 'error' Event in Node.js HTTP Server

This repository demonstrates a common error in Node.js HTTP servers: failure to handle the 'error' event, leading to server crashes upon abrupt client disconnections.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

The `bug.js` example creates a simple HTTP server.  If a client abruptly disconnects (e.g., by closing the browser tab), the server crashes without providing informative error messages. This makes debugging difficult.

## Solution

The `bugSolution.js` file addresses this by adding an 'error' event listener to the server. This listener gracefully handles errors, logs them to the console, and prevents the server from crashing.  Best practice is to incorporate robust error handling in production environments.