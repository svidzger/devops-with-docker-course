# Start from the ubununtu 22.04 image
FROM ubuntu:22.04

# Use /usr/src/app as our workdir
WORKDIR /usr/src/app

# Copy the hello.sh file
COPY script.sh .

# Instructions to install curl
RUN chmod +x script.sh && apt-get update && apt-get install -y curl

# When running Docker run the command will be ./script.sh
CMD ./script.sh
