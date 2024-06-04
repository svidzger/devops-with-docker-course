# Eclipse temurin java 8
FROM eclipse-temurin:8-jdk

# Expose port 8080
EXPOSE 8080

# Set the working directory
WORKDIR /usr/src/app

# Copy the project files to the container
COPY . .

# Build the project
RUN ./mvnw package

# Run app
CMD ["java", "-jar", "/usr/src/app/target/docker-example-1.1.3.jar"]

