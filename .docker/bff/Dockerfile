FROM node:alpine as build

WORKDIR /i-recipe

COPY ./package.json .
COPY ./packages/bff/package.json ./packages/bff/

RUN yarn install --pure-lockfile --non-interactive --production

COPY ./packages/bff/dist ./packages/bff/

ENV NODE_ENV production

WORKDIR /i-recipe/packages/bff

EXPOSE 3000

CMD ["node", "main"]