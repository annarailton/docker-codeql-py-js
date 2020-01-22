# docker-codeql-py-js

A minimal docker container that contains all you need to:

* build both Python and JavaScript `codeql` databases 
* run `codeql` over Python and JavaScript databases

## Information

* Information on how to install [Docker](https://www.docker.com/)
* Based on Python (3.7-slim-stretch) official Image [python:3.7-slim-stretch](https://hub.docker.com/_/python/) 
* [LTS version of `node.js`](https://hub.docker.com/_/node)
* Information about [`codeql`](https://securitylab.github.com/tools/codeql)

## Installation

Pull the image from the Docker repository.

```bash
docker pull annarailton/codeql-py-js
```

## Build

This uses a chain of docker images, starting from `node:lts-slim`. 
```bash
docker build -t annarailton/node-lts-python3.7-slim node-lts-python3.7-slim
docker build -t annarailton/node-lts-python3.7-slim-codeql .
```

Or 
```bash
docker build -t annarailton/codeql-py-js https://github.com/annarailton/docker-codeql-py-js.git
```
