# Use the official Node.js 14 image as the base image
FROM node:14

# Set the working directory inside the container
WORKDIR /app

# Copy the package.json and package-lock.json files to the working directory
COPY package*.json ./

# Install the dependencies
RUN npm install

# Copy the entire client directory to the working directory
COPY . .

# Build the client application
RUN npm run build

# Expose port 3000 for the client application
EXPOSE 3000

# Set the command to start the client application
CMD ["npm", "start"]

# Set the environment variable API_BASE
ENV API_BASE="http://localhost:9000"

# Expose the port
EXPOSE 3000

# Start the client application
CMD ["npm", "start"]
