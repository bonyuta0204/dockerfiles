# Use the official Debian image as the base
FROM debian:bullseye-slim

# Set environment variables for non-interactive installation
ENV DEBIAN_FRONTEND=noninteractive

# Install dependencies
RUN apt-get update && \
    apt-get install -y \
    curl \
    gnupg2 \
    ca-certificates \
    build-essential \
    gdb \
    python3 \
    git \
    pkg-config \
    libssl-dev \
    && rm -rf /var/lib/apt/lists/*

# Shallow clone Node.js source code (version 20.x)
RUN git clone --depth 1 --branch v20.x https://github.com/nodejs/node.git


# Build Node.js with debug symbols
RUN cd node && \
    ./configure --debug && \
    make -j$(nproc) && \
    make install

# Clean up unnecessary files to reduce image size
RUN apt-get remove -y git && \
    apt-get autoremove -y && \
    rm -rf /var/lib/apt/lists/* /node

# Set working directory
WORKDIR /app

# Default command (you can replace it with your app entry point)
CMD ["bash"]
