FROM node:14

WORKDIR /usr/src/app
COPY package.json ./
COPY yarn.lock .
RUN yarn install --production
COPY app.js .
COPY ./config ./config
COPY ./models ./models
COPY ./routes ./routes

EXPOSE 3000

ENTRYPOINT sleep 30 && yarn start
