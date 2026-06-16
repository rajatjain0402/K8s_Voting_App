FROM node:18-alpine

WORKDIR /app

# dependencies install
COPY package*.json ./
RUN npm install

# code copy
COPY . .

EXPOSE 80

CMD ["node", "server.js"]