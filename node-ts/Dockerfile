FROM node:latest as node

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

RUN npm run build

EXPOSE 80
CMD [ "node","--max_old_space_size=16384", "./dist/server.js" ]