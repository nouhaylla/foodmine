# Use Node.js image
FROM node:16.14 AS build

# Set working directory
WORKDIR /frontend

# Copy package.json and package-lock.json
COPY package.json package-lock.json /frontend/

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . /frontend/

# Build the Angular app
RUN npm run build

# Expose port 4200 (assuming your app runs on this port)
EXPOSE 4200

# Command to run the Angular app
CMD ["npm", "start"]
