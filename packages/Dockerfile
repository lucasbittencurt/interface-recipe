FROM node:alpine as production

WORKDIR /usr/app

COPY . .

RUN npm install
RUN npm run build

EXPOSE 3333

CMD [ "npm", "start:prod" ]