# Use the official Nginx image based on Alpine Linux for a lightweight container
FROM nginx:alpine 

# Set the working directory inside the container to /usr/share/nginx/html
WORKDIR /usr/share/nginx/html 

# Copy all files from the current directory (on the host) to the working directory in the container
COPY . . 

# Expose port 80 for the container, making it accessible to the outside world
EXPOSE 80



after that

to create image from Dockerfile write command
docker build -t (your image name)
## Dockerfile for Nginx Web Server

This Dockerfile uses the official Nginx image based on Alpine Linux for a lightweight container.

```dockerfile
# Use the official Nginx image based on Alpine Linux for a lightweight container
FROM nginx:alpine 

# Set the working directory inside the container to /usr/share/nginx/html
WORKDIR /usr/share/nginx/html 

# Copy all files from the current directory (on the host) to the working directory in the container
COPY . . 

# Expose port 80 for the container, making it accessible to the outside world
EXPOSE 80
```

### Instructions

1. **Build the Docker Image**  
   To create an image from the Dockerfile, run the following command:
   ```bash
   docker build -t your-image-name .
   ```

2. **Run the Docker Container**  
   To convert the image into a container, use the following command:
   ```bash
   docker run -td --name your-container-name -p 80:80 your-image-name
   ```

Replace `your-image-name` and `your-container-name` with your desired names.


then,to convert image into container write
docker run -td --name (name of container) -P 80:80 (name of image)





