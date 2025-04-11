# Docker_part1
Step 1:
I first create the node.js app that respond with the "Hello Aleesha" on localhost:3000
code is:
// index.js
const express = require('express');
const app = express();
const port = 3000;


app.get('/', (req, res) => {
  res.send('Hello Aleesha!');
});

// Start the server
app.listen(port, () => {
  console.log(`Server running at http://localhost:${port}`);
});

