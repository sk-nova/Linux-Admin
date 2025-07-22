# Use the official Ubuntu base image
FROM ubuntu:latest

# Prevent prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive

# Update package list and install desired packages (e.g., curl, vim, git)
RUN apt update && \
    apt install -y \
    sudo \
    vim \
    curl \
    git \
    net-tools \
    iproute2 \
    openssh-server \
    systemd && \
    apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Set default command to bash
CMD ["/bin/bash"]
