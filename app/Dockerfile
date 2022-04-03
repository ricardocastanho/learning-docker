FROM node:14.16.0-alpine3.13

# Create app directory
WORKDIR /home/node

# Install app dependencies
COPY package.json yarn.lock ./

RUN yarn install

# Bundle app source
COPY ./src ./src

EXPOSE 3000

CMD [ "yarn", "nodemon", "src/server.js" ]
