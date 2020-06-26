FROM node:14 AS build

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install
COPY ./src ./src
COPY ./public ./public

RUN npm run build

FROM node:14

RUN npm -g install serve
COPY --from=build /usr/src/app/build /build

EXPOSE 5000

CMD [ "serve", "-s", "build" ]
