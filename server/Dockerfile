# Use official Node.js 14 as base image
FROM node:current-slim

# Set working directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the server code
COPY . .

# Expose port 3000 for the server
EXPOSE 5000

# Start the server
CMD [ "npm", "start" ]