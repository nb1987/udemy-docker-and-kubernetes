# get base image 
FROM node:alpine

# establish working directory, so all subsequent commands will be run relative to the WORKDIR
WORKDIR /usr/app

# Copy from current working directory to container
COPY ./ ./

# install node app dependencies
RUN npm install

# execute start-up command to spin up web server
CMD ["npm", "start"]
