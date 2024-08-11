# question: when I ask copilot to optimse this code suggect to use node14 to have a smaller image size should I do this changes? and how we know which version should I use


# Stage 1: Build the react client
From node:20.10.0-alpine As ui-build

WORKDIR /app

COPY package*.json ./
RUN npm ci

COPY . .
RUN npm run build

# Stage 2: Serve the react client with nginx
From nginx:1.21.3-alpine

COPY --from=ui-build /app/build /usr/share/nginx/html

EXPOSE 80

CMD [ "nginx", "-g" ,"daemon off;" ]

