# Base image
FROM node:6-alpine

# Default port of container based on this image
EXPOSE 3000

# Install Tini
RUN apk add --no-cache tini

#WORK DIRECTORY
WORKDIR /usr/src/app

# Copy package.json to WorkDir
COPY package.json package.json

# Install packages and clean cache
RUN npm install && npm cache clean --force

# Copy all files in Work directory
COPY . .

# Command to launch server
CMD ["npm", "start"]