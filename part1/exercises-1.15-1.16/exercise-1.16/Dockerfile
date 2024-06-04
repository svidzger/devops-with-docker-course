# Use Node 16 from Docker Hub
FROM --platform=linux/amd64 node:16-buster

# Expose port 5001
EXPOSE 5001

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Install the `serve` package globally to serve the app
RUN npm install -g serve

# Copy the project files to the working directory
COPY . .

# Build the React app
RUN npm run build

# Command to run the app using `serve`
CMD ["serve", "-s", "-l", "5001", "build"]
