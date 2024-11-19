# Use the lightweight official NGINX image
FROM nginx:alpine

# Set environment variables for better behavior
ENV NGINX_VERSION=1.24.0

# Copy a custom NGINX configuration file
COPY nginx.conf /etc/nginx/nginx.conf

# Ensure permissions are correctly set for security
RUN chmod 644 /etc/nginx/nginx.conf

# Expose the HTTP port
EXPOSE 80

# Use NGINX default command to start the server
CMD ["nginx", "-g", "daemon off;"]
