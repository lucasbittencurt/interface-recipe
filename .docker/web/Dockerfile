FROM node:alpine as build

# Set working directory
WORKDIR /i-recipe

# Install PM2 globally
# RUN npm install --global pm2

# Copy "package.json" and "package-lock.json" before other files
# Utilise Docker cache to save re-installing dependencies if unchanged
COPY ./package.json .
COPY ./packages/web/package.json ./packages/web/

# Install dependencies
RUN yarn install

# Copy all files
COPY ./packages/web/ ./packages/web/

# RUN cd node_modules
# RUN ls -la
# RUN cd ..
WORKDIR /i-recipe/packages/web
# RUN ls -la

# Build app
RUN yarn build

# WORKDIR /i-recipe/packages/web/node_modules
# RUN ls -la

# Expose the listening port
FROM node:alpine
WORKDIR /i-recipe
COPY --from=build /i-recipe .
WORKDIR /i-recipe/packages/web
RUN ls -la
EXPOSE 3000
CMD ["node_modules/.bin/next", "start"]