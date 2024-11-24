# OpenCTI - amd64 to arm64

This repository contains instructions and resources for deploying [OpenCTI](https://github.com/OpenCTI-Platform/opencti) on ARM64 architecture. The guide provides a comprehensive walkthrough for converting and running OpenCTI, originally designed for `amd64`, on `arm64` platforms.

## Overview

OpenCTI is an open-source platform for cyber threat intelligence analysis and sharing. This repository is focused on making OpenCTI compatible with ARM64 architecture, allowing users to deploy it on ARM-based systems like Raspberry Pi, AWS Graviton, or any other ARM64 environment.

## Features

- ARM64 compatibility for OpenCTI
- Step-by-step conversion and deployment guide
- Docker support for ARM64
- Pre-built Docker images (if available)
- Instructions for building from source on ARM64

## Prerequisites

To get started, ensure you have the following:

- An ARM64 environment (e.g., Raspberry Pi, ARM64 VM, AWS EC2 with ARM)
- [Docker](https://docs.docker.com/get-docker/) installed
- [Docker Compose](https://docs.docker.com/compose/install/) installed
- Git installed
- Basic knowledge of Docker and Docker Compose

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/imaltaf/opencti-arm64.git
cd opencti-arm64
```

### 2. Build the Docker Images for ARM64

If you want to build the Docker images from scratch:

```sh
docker-compose -f docker-compose-arm64.yml build
```
Alternatively, if pre-built ARM64 Docker images are available:

```sh
docker-compose -f docker-compose-arm64.yml pull
```
### 3. Run the Containers

Once the images are ready, you can start the services using Docker Compose:

```sh
docker-compose -f docker-compose-arm64.yml up -d
```

### 4. Access OpenCTI

OpenCTI should now be running on your ARM64 device. You can access it via a web browser:

```sh
http://localhost:8080
```

# Building from Source

To build OpenCTI from source on an ARM64 system:

## Install Dependencies:

Follow the OpenCTI official documentation to install required dependencies like Node.js, Python, and other tools compatible with ARM64.

Build and Run:

Clone the official OpenCTI repository and build it using the standard build instructions, ensuring the environment is ARM64 compatible.

Troubleshooting
Here are some common issues and solutions when running OpenCTI on ARM64:

Performance Issues: Ensure your ARM64 environment has sufficient CPU and memory resources.
Build Failures: Double-check that all dependencies are correctly installed for ARM64.
Docker Compatibility: Some OpenCTI dependencies might require specific ARM64-compatible Docker images. Modify the Dockerfile accordingly if needed.
Contributing
Contributions are welcome! If you encounter any issues or have suggestions for improvement, feel free to open an issue or submit a pull request.

## License
This project is licensed under the MIT License.

## Acknowledgements
Special thanks to the OpenCTI team for their excellent work on the OpenCTI platform.

## Contact
For questions, suggestions, or feedback, feel free to reach out:

GitHub: imaltaf
Email: altaf@codesec.me
