# Use an official node image as a base
FROM node:14-alpine

# Set the working directory in the container
WORKDIR /app

# Copy package.json and package-lock.json
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application files
COPY . .

# Build the React application
RUN npm run build

# Install a simple server to serve the built files
RUN npm install -g serve

# Expose the port the app will run on
EXPOSE 5000

# Command to run the application
CMD ["serve", "-s", "build", "-l", "5000"]



