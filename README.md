# Node.js Server Hang on Long Requests

This repository demonstrates a common issue in Node.js where long-running requests can cause the server to hang, becoming unresponsive to other requests.  The `server.js` file shows the problematic code, while `server-solution.js` provides a solution using asynchronous operations.

## Problem

The original code uses a `while` loop to simulate a 5-second delay within the request handler. This blocks the event loop, preventing Node.js from processing other incoming requests.  The server appears to hang or freeze.

## Solution

The solution utilizes asynchronous operations (setTimeout) to avoid blocking the event loop.  The server remains responsive even while processing long-running tasks.

## How to run

1. Clone this repository.
2. Navigate to the repository directory in your terminal.
3. Run `node server.js` to see the hanging behavior.
4. Run `node server-solution.js` to see the improved responsive behavior.