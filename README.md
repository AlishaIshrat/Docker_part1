# Docker_part1
Step 1: Identify the Sample Application
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
Step 2: Identify the dependencies 
 dependencies to move the app into a docker container.
``` javascript

package.json ( list all dependencies)
npm install  (create node module container contain actual code for express)

```
Step 3: Create the Docker file
I first created the Dockerfile with no extension in VS code then it created the file named with "Dockerfile" in VS Code
Code for creating the Dockerfile 
```javascript
FROM node:18-alpine

WORKDIR  /app

COPY package*.json ./


RUN npm install

COPY . .

EXPOSE 3000

CMD ["node", "index.js"]

```
Using the 18 version of node with alpine which is super lightweight. This sets the base image FROM node:18-alpine.

Step 4: Build the Docker Image
The command:
```javascript
docker build -t first-image .
```
to build the docker image named "first-image"

I first created this image with upper-case letter after getting error I recognized that it should be in lowercase.

Step 5: Push Docker Image to Docker Hub
For pushing the docker Image I first downloaded the docker hub.

