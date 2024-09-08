FROM node:20.10.0-alpine As server-build


WORKDIR /app

COPY package*.json ./

RUN npm ci --omit=dev

COPY . .

EXPOSE 4000

CMD ["npx", "ts-node", "src/index.ts"]
