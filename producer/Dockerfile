# Use the official Go image as the base image
FROM golang:1.17

# Set the working directory inside the container
WORKDIR /app

# Copy the Go module files and download the dependencies
COPY go.mod go.sum ./
RUN go mod download

# Copy the rest of the application code
COPY . .

# Build the Go application
RUN go build -o producer .

# Set the command to run the producer binary when the container starts
CMD ["./producer"]