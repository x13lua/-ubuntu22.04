# Ubuntu 22.04 QEMU Virtual Machine in Docker Container

![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=for-the-badge&logo=qemu&logoColor=white)

A lightweight Ubuntu 20.04 virtual machine running in a Docker container using QEMU/KVM for optimal performance.

## Features

- 🐳 Containerized Ubuntu 22.04 VM
- ⚡ KVM-accelerated for near-native performance
- 🌐 Web-based VNC access (port 6080)
- 🔑 SSH access (port 2221)
- 💾 Persistent storage volume

## Prerequisites

- Docker installed
- KVM support on host machine
- `sudo` privileges (for KVM device access)


 ## VM user and pass
 - username:- root
 - password:- root

## Installation

```bash
# Clone the repository
git clone https://github.com/hopingboyz/ubuntu22.04
cd ubuntu22.04

# Build the Docker image
docker build -t ubuntu-vm .

# Run the container

docker run --privileged -p 6080:6080 -p 2221:2222 -v $PWD/vmdata:/data ubuntu-vm
