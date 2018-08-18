<h1 align="center">Docker compose Node.js boilerplate</h1>
<p align="center">This is a Docker Compose boilerplate for Node.js with yarn, based on Alpine Linux image</p>
<p align="center">
  <img width="150" height="150" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQWDWWMBh8n7MPfnXSxV7u6XGLybLQNrF52NjoemwP1iLPqwnkMQQ" alt="Linux Alpine logo">
  <img width="150" height="150" src="https://nodejs.org/static/images/logo-light.svg" alt="Node.js logo">
  <img width="150" height="150" src="https://yarnpkg.com/assets/search/ico-yarn.svg" alt="Yarn logo">
  <img width="150" height="150" src="https://raw.githubusercontent.com/docker/compose/master/logo.png" alt="Docker compose logo">
</p>

---

## Into:
This docker Node.js boilerplate is a wrapper of [docker hub image](https://hub.docker.com/_/node/) with installed `yarn` as a package manager.

## Installation:
1. Clone repository:
<pre class="command-line">
    <span class="command">git clone https://github.com/EliFuzz/docker-nodejs-boilerplate.git</span>
</pre>
2. Go to folder:
<pre class="command-line">
    <span class="command">cd docker-nodejs-boilerplate</span>
</pre>
3. Copy and rename `.env_bak` to `.env`:
<pre class="command-line">
    <span class="command">cp .env_bak .env</span>
</pre>
4. Build docker:
<pre class="command-line">
    <span class="command">docker-compose up -d</span>
</pre>
5. Install NPM dependencies (only once):
<pre class="command-line">
    <span class="command">docker-compose exec dev sh -c "yarn"</span>
</pre>
6. Run NPM start script:
<pre class="command-line">
    <span class="command">docker-compose exec dev sh -c "yarn start"</span>
</pre>
7. Exit docker:
<pre class="command-line">
    <span class="command">docker-compose down</span>
</pre>


## Settings:
`.env`:
- NODE_PORT=**3000**
- NODE_ENV=**development**

`docker/dev/Dockerfile`:
- FROM node:**10.9.0**-alpine - you can change node version. Look for reference: [Docker Hub](https://hub.docker.com/_/node/)
