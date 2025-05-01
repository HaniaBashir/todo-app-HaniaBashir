# Use the latest official Node.js image
FROM node:latest

# Set the working directory for the frontend
WORKDIR /app

# Copy the frontend package.json and package-lock.json for installing dependencies
COPY frontend/package*.json ./

# Install frontend dependencies
RUN npm install

# Copy the frontend source code into the container
COPY frontend/ .

# Build the React app for production
RUN npm run build

# Install a simple HTTP server to serve the production build
RUN npm install -g serve

# Expose port 3000 for the frontend
EXPOSE 3000

# Serve the app on port 3000
CMD ["serve", "-s", "build", "-l", "3000"]
