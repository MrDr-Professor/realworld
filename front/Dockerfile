FROM node:14 AS build

ARG app_api=http://localhost:3000/api
WORKDIR /usr/src/app
ENV REACT_APP_API=http://bootcamp-demo.toolchain.lead.sandbox.liatr.io:3000/api

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
