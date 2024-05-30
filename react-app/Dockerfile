# Use an official Node.js runtime as the base image
FROM node:18.12.1

RUN apt-get update && apt-get install -y openssl ca-certificates
# Set the working directory
WORKDIR /app

RUN chmod -R 777 /app
# Copy the package.json and package-lock.json first
COPY package.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code
COPY . .

# Expose port 3000 and start the app
EXPOSE 3000
CMD ["npm", "start"]
