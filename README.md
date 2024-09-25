# Debounced Sum Calculator

This project demonstrates debouncing in JavaScript. Users input two numbers, and the sum is calculated using an external API with debouncing to prevent frequent API calls while typing.

## What is Debouncing?

Debouncing delays the execution of a function until a specified time has passed after the last event. It helps optimize performance by reducing the number of function calls.

## Features

- **Debounced Input**: Sum is calculated after 300ms of inactivity.
- **Async API Call**: Fetches the sum from a server and displays it.

## Usage

1. Clone the repository.
2. Set up a local server for the sum API (example below).
3. Open `index.html` in a browser.
4. Enter two numbers to see the debounced sum.

### Example API Setup

```javascript
const express = require("express");
const app = express();
const port = 3000;

app.get("/sum", (req, res) => {
  const { a, b } = req.query;
  const sum = Number(a) + Number(b);
  res.send(sum.toString());
});

app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}`);
});
```
