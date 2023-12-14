# Use a base image that supports running the client application
FROM node:14

# Set the working directory
WORKDIR /app

# Copy package.json and package-lock.json
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy the entire contents of the src directory
COPY src/ ./src/

# Set the environment variable API_BASE
ENV API_BASE="http://localhost:9000"

# Expose the port
EXPOSE 3000

# Start the client application
CMD ["npm", "start"]
