# Use official Node.js 14 as base image
FROM node:current-slim

# Set working directory
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the client code
COPY . .

RUN mv .env.example .env

# Build the client for production
RUN npm run build

# Expose port 8080 for the client
EXPOSE 3000

# Start the client
CMD [ "npm", "run", "dev", "--", "--host", "0.0.0.0" ]