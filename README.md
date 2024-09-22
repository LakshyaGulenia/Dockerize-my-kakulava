# Use the official Nginx image based on Alpine Linux for a lightweight container
FROM nginx:alpine 

# Set the working directory inside the container to /usr/share/nginx/html
WORKDIR /usr/share/nginx/html 

# Copy all files from the current directory (on the host) to the working directory in the container
COPY . . 

# Expose port 80 for the container, making it accessible to the outside world
EXPOSE 80
