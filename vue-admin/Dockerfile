# base image
FROM node:lts-alpine

RUN apk add --no-cache \
  git \
  openssh
  
RUN npm install -g  http-server @vue/cli vue  nodemon grunt npm-check-updates
 
# set working directory
RUN mkdir /app

ADD ["./vue-admin/package.json", "/app"]
WORKDIR /app
RUN npm install --verbose

WORKDIR /app

# start app
CMD ["npm", "run", "serve"]
