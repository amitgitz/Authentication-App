# Use the official Node.js image as the base image
FROM node:14-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json (or yarn.lock) files to the working directory
COPY package*.json ./

# Install app dependencies
RUN npm install --production

# Copy the entire backend app to the working directory
COPY . .

# Expose the port that your Node.js app will listen on
# Replace 3000 with the actual port your Node.js app uses
EXPOSE 3000

# Command to start your Node.js app
# Modify this based on the start command of your backend app
CMD ["npm", "start"]

