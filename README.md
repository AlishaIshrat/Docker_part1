# Docker_part1
Step 1:
I first create the node.js app that respond with the "Hello Aleesha" on localhost:3000
code is:
```javascript

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
```
Step 2:
Identify the dependencies to move the app into a docker container.
``` javascript

package.json ( list all dependencies)
npm install  (create node module container contain actual code for express)

```
