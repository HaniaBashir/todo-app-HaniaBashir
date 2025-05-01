# Use the latest official Node.js image
FROM node:latest

# Set the working directory for the backend
WORKDIR /app

# Copy the backend package.json and package-lock.json for installing dependencies
COPY backend/package*.json ./

# Install backend dependencies
RUN npm install

# Copy the rest of the backend code
COPY backend/ .

# Expose port 5000 for the backend
EXPOSE 5000

# Command to run the backend application
CMD ["npm", "start"]
