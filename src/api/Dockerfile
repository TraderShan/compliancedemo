FROM node:22-alpine

WORKDIR /app

COPY package*.json ./
RUN npm ci --omit=dev && test -d node_modules/express

COPY . .

EXPOSE 8080

CMD ["node", "server.js"]
