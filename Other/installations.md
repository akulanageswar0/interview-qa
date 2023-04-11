Installation instructions for Node.js v19.x:

```bash
Using Ubuntu:
curl -fsSL https://deb.nodesource.com/setup_19.x | sudo -E bash - &&\
sudo apt-get install -y nodejs

Using Ubuntu, as root
curl -fsSL https://deb.nodesource.com/setup_19.x | bash - &&\
apt-get install -y nodejs
```
# NodeJS usage
node -v && npm -v


## Create a directory


```bash
mkdir test && cd test
```

## Next, create a package.json file

```{
  "name": "docker_nodejs_app",
  "version": "1.0.0",
  "description": "Node.js on Docker",
   "license": "MIT",
  "main": "server.js",
  "scripts": {
    "start": "node server.js"
  },
  "dependencies": {
    "express": "^4.16.4"
  }
}
```

```bash
npm install
```

## create a server.js 

``` bash
var http = require('http');
var handleRequest = function(request, response) {
  response.writeHead(200);
  response.end("Hello world");
}
var www = http.createServer(handleRequest);
www.listen(8080);
```
```
node server.js
```
### Open browser and check the localhost:8080

## Dockerfile sample for nodejs

```bash
FROM node:8
WORKDIR /usr/src/app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 8080
CMD [ "npm", "start" ]
```
```bash
docker build -t gpreddyjgl/nodejstest .
```
