FROM node:14

WORKDIR /usr/src/app
COPY package.json ./
COPY yarn.lock .
RUN yarn install
COPY . .

EXPOSE 3000

ENTRYPOINT sleep 30 && yarn start
