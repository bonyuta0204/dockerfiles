# Dockerfiles Collection

This repository contains a collection of Dockerfiles for various use-cases

## Prerequisites

- Docker: Ensure that Docker is installed on your machine before proceeding. You can download and install it from [Docker's official website](https://www.docker.com/products/docker-desktop).

## Why This Repository Exists

Managing multiple Dockerfiles for different scenarios can become tedious. This repository aims to become a one-stop solution for me and anyone interested, providing ready-to-use Dockerfiles that can be built into Docker images easily.

## Dockerfiles Included

### Ruby2.7-Node14.18-Alpine
- **Use-Case**: Docker image with Ruby and Node
- **Directory**: `ruby2.7-node14.18-alpine`

### AutoGPT
- **Use-Case**: Docker image for running AutoGPT
- **Directory**: `AutoGPT`

## How to Use

1. **Clone the Repository**
    ```bash
    git clone https://github.com/bonyuta0204/dockerfiles.git
    ```

2. **Navigate to the Dockerfile Directory**
    ```bash
    cd dockerfiles/[Specific Dockerfile Directory]
    ```

3. **Build the Docker Image**
    ```bash
    docker build -t [image-name] .
    ```

## Contributing

While this repository is primarily for personal use, contributions are welcome. Feel free to fork the repository and submit pull requests.

## Author

- **bonyuta0204**


