![Interface Recipe](https://raw.githubusercontent.com/lbittencurt/interface-recipe/3961fb162cd8edda582eda3116326ce364378466/assets/interface_recipe_logo.svg)

This is a boilerplate to be used to build React web applications with a Node BFF (Backend for Frontend).

## What is inside?
- Workspace
  - Typescript
  - Jest
  - Eslint
  - Prettier
  - Husky
  - Docker
- Web
  - NextJS
  - Styled Components
  - React Testing Library
  - Plop
- BFF
  - NestJS
  - Rxjs
  - supertest

## Development Structure
This project have a docker-compose file to build and run the development environment. Using Dockerfiles that are in `.docker` package.

## Production Structure
🔬 Todo

## Prerequisites
- Docker
- Docker-compose
- Nodejs

## Getting started
```
# clone boilerplate
# install dependencies
yarn

# build docker environment
yarn dev:build

# run docker environment
yarn dev:run
```
