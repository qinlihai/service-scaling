# Use a minimal base image like Alpine Linux or Debian for a lightweight container
FROM alpine:latest

# Install necessary dependencies (e.g., GCC for compiling C code, libraries)
RUN apk add --no-cache gcc musl-dev make

# Set the working directory in the container
WORKDIR /app

# Copy the source code into the container
COPY . .

# Compile the C code (assuming main.c is the main file)
RUN gcc -o my-service main.c

# Expose the port the service listens on (e.g., 8080)
EXPOSE 8080

# Set the default command to run the service
ENTRYPOINT ["./my-service"]
