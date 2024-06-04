# Use Go 1.16 from Docker Hub
FROM golang:1.16

# Expose the application on port 8080
EXPOSE 8080

# Set the working directory inside the container
WORKDIR /usr/src/app

# Copy the source code into the working directory
COPY . .

# Download necessary Go modules and dependencies
RUN go mod download

# Run tests
RUN go test ./...

# Set environment variables
ENV REQUEST_ORIGIN=http://localhost:5001

# Build the Go project
RUN go build -o server .

# Command to run the compiled server
CMD ["./server"]


