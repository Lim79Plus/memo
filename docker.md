# docker

### dockerfile example for node.js
```
#docker run -it node:8.15-alpine sh
FROM node:8.15-alpine

RUN mkdir src

WORKDIR /src

ADD app.js ./
ADD package.json ./
ADD package-lock.json ./
ADD node_modules ./node_modules

EXPOSE 3000
CMD ["node", "/src/app.js"]
```

### docker cmd
##### copy from container to local
```
// check container id
docker ps -a

// copy from container to local directory
docker cp <container ID>:/etc/my.cnf my.cnf
```
