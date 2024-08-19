FROM mcr.microsoft.com/devcontainers/universal:2-linux
# Install the xz-utils package
RUN apt-get update && \
pip install django

# Install MongoDB
RUN apk add --no-cache mongodb
