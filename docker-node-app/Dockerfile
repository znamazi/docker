FROM node:20.10.0-alpine As server-build

WORKDIR /app/server

COPY package*.json ./

RUN npm ci

COPY . .

EXPOSE 5000

CMD [ "node","index.js" ]