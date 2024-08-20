FROM mcr.microsoft.com/devcontainers/universal:2-linux

# Install the xz-utils package and MongoDB
RUN apt-get update && \
    apt-get install -y xz-utils mongodb && \
    pip install django

# Create the MongoDB data directory
RUN mkdir -p /data/db

# Expose ports for Django and MongoDB
EXPOSE 8000 27017

# Command to run MongoDB
CMD ["mongod", "--bind_ip_all"]
