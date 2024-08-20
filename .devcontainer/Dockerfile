FROM mcr.microsoft.com/devcontainers/universal:2-linux

# Install the xz-utils package, MongoDB, and Node.js
RUN apt-get update && \
    apt-get install -y xz-utils mongodb && \
    curl -fsSL https://deb.nodesource.com/setup_18.x | bash - && \
    apt-get install -y nodejs && \
    pip install django

# Install Next.js globally
RUN npm install -g create-next-app

# Create the MongoDB data directory
RUN mkdir -p /data/db

# Expose ports for Django, MongoDB, and Next.js
EXPOSE 8000 27017 3000

# Command to run MongoDB
CMD ["mongod", "--bind_ip_all"]
