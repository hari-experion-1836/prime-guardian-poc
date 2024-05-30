# Use an official Node.js runtime as the base image
FROM node:20

# Set the working directory
WORKDIR /app

# Copy the package.json (and package-lock.json if it exists)
COPY package.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose port 5000 and start the app
EXPOSE 5000
CMD ["npm", "start"]
