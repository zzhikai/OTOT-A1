FROM node:16

# Create app directory
WORKDIR /Users/zhikaizhang/zzhikai/OTOT-A1/app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
# where available (npm@5+)
COPY package*.json ./

RUN npm install
# If you are building your code for production
# RUN npm ci --only=production

# Bundle app source code inside the Docket image with COPY instruction
COPY . .

# Given app binds to port 3000 as defined in index.js/server.js, use EXPOSE instruction
# to have it mapped by the docker daemon
EXPOSE 3000

# Define command to run your app using CMD which defines your runtime
# We will use node index.js to start the server:
CMD [ "node", "index.js" ]a

# Ensure .dockerignore file is created in the same directory as Docketfile
# With the following: 
# node_modules
# npm-debug.log
# This will prevent your local modules and debug logs from being copied 
# onto your Docker image and possibly overwriting modules installed within your image.

# Building the docker image
# Go to the directory with your Dockerfile and run the following command
# -t flag lets you tag your image so it's easier to find later using the docker images command:
# docker build . -t <your username>/node-web-app .

# How to run the image
# Running the image with -d runs the container in detached mode,
# leaving the container running in the background.
# The -p flag redirects a public port to a private port inside the container.
# Run the image you previously built:
# docker run -p 49160:8080 -d <your username>/node-web-app