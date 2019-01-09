# get base image 
FROM node:alpine

# establish working directory, so all subsequent commands will be run relative to the WORKDIR
WORKDIR /usr/app

# Copy package.json first, so that the ONLY time Docker caching behavior needs to run npm install again - 
# rather than fetch existing intermediate images - is when package.json changes
COPY ./ ./

# install node app dependencies
RUN npm install

# copy all files from current working directory to container
COPY ./ ./

# execute start-up command to spin up web server
CMD ["npm", "start"]
