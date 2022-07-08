FROM nginx:alpine

RUN mkdir -p /home/node/app/node_modules

WORKDIR /home/node/app

COPY package*.json ./

RUN apk add --update nodejs npm

RUN npm install

COPY . .

EXPOSE 3001

CMD [ "npm", "start" ]