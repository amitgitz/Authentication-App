# Use the official Node.js image as the base image
FROM node:14-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json (or yarn.lock) files to the working directory
COPY package*.json ./

# Install app dependencies
RUN npm install

# Copy the entire frontend app to the working directory
COPY . .

# Build the production version of the frontend app
RUN npm run build

# Expose the port that the frontend app will listen on (if applicable)
# This should be the same port you specified in your React app
EXPOSE 3000

# Command to run your frontend app (modify if necessary)
CMD ["npm", "start"]

