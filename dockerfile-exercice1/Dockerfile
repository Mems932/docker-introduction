FROM node:18-alpine

WORKDIR /app

COPY package*.json ./

RUN npm install && npm install -g serve

COPY src ./src
COPY public ./public

RUN npm run build && rm -fr node_modules

EXPOSE 3000

CMD ["serve", "-s", "build"]