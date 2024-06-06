# Use the official Node.js 20 image as the base image
FROM node:20

# Set the working directory to /app
WORKDIR /frontend

# Copy package.json and package-lock.json (if available)
COPY package*.json ./

# Install dependencies
RUN npm install \
    && npm install nodemon \
    && npm install ts-node

# Copy the rest of the application code
COPY . .

# Change directory to src
WORKDIR /frontend/src

EXPOSE 5000

    # Command to run the application
CMD ["npx", "nodemon", "server.ts"]
