# Bugs In My Life

I will add bugs and solutions here that I have faced in my Software Engineering Life (which is too small just like your dick :3)

## Docker

#### Problem | Error

`gyp ERR! find Python` on **node alpine** image (specially on `node:14-alpine`)

##### How to produce

[sample dockerfile and package.json file](./gyp_err_find_python/)

##### Solution

add `RUN apk add --no-cache python3 py3-pip make g++` before npm install command.

##### Explanation

- [Document how to use alpine with dependencies that rely on node-gyp](https://github.com/nodejs/docker-node/issues/282)
  
- [docker-alpine-usage](https://github.com/gliderlabs/docker-alpine/blob/master/docs/usage.md)
