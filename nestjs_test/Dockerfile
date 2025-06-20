FROM node:18 AS build

WORKDIR usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

# stage of point
FROM node:18-alpine3.19

WORKDIR usr/src/app

COPY ---from=build usr/src/app/package*.json ./package.json
COPY ---from=build usr/src/app/ ./dist
COPY ---from=build usr/src/app/node_modules ./node_modules


EXPOSE 3000

CMD ["npm", "run", "start:prod"]