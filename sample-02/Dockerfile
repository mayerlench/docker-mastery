FROM node:10-alpine

EXPOSE 3000
RUN apk add --update curl

WORKDIR /usr/src/app

# The * will copy the file only if its there
COPY package.json package-lock.json* ./ 
RUN npm install && npm cache clean --force

COPY . .

CMD [ "node", "./bin/www" ]
