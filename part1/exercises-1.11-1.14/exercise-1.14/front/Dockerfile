# Use Node 16 from Docker Hub
FROM node:16-buster

# Expose port 5001
EXPOSE 5001

# Set the working directory
WORKDIR /usr/src/app

# Copy package.json and package-lock.json to the working directory
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the project files to the working directory
COPY . .

# Set environment variable for backend URL
ENV REACT_APP_BACKEND_URL=http://localhost:8080

# Build the React app
RUN npm run build

# Install the `serve` package globally to serve the app
RUN npm install -g serve

# Command to run the app using `serve`
CMD ["serve", "-s", "-l", "5001", "build"]
