FROM node:14

WORKDIR /usr/src/app

COPY package*.json ./
RUN npm install --production
COPY ./src ./src
COPY ./public ./public

EXPOSE 8080

CMD [ "npm", "start" ]
