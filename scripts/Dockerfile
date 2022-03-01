FROM node:16.13-alpine3.15

# Create app directory
WORKDIR /usr/src/app

# Install app dependencies
COPY my_app/package*.json ./

RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source
COPY my_app .


EXPOSE 8080
CMD [ "node", "server.js" ]
