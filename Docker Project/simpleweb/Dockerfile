# Set the base image
FROM node:18-alpine

# Set the workingg directory
WORKDIR /usr/app

# Copy package.json into the container
COPY ./package.json ./

# Install dependencies
RUN npm install

# Copy the rest of the  files
Copy ./ ./

# Start the web server
CMD [ "npm", "start" ]