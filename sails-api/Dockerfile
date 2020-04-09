FROM node:10.18.0

RUN npm install -g sails nodemon pm2 grunt npm-check-updates

RUN ["mkdir", "/app"]

ADD ["./sails-api/package.json", "/app"]
WORKDIR /app
RUN npm install --verbose

WORKDIR /app
