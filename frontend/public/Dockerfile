# Use the official Nginx image as a parent image
FROM nginx:latest

# Copy the contents of the 'public' folder to the default Nginx public directory
COPY frontend/public/index.html /usr/share/nginx/html
COPY frontend/public/nginx.conf /etc/nginx/conf.d/default.conf


EXPOSE 8080
