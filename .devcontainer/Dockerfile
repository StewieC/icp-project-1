# Start from the GitHub Codespaces base image
FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Install curl, build essentials
RUN apt-get update && apt-get install -y \
    curl build-essential libssl-dev pkg-config

# Install dfx
RUN curl -fsSL https://internetcomputer.org/install.sh | sh

ENV PATH="/root/bin:${PATH}"

# Install Node.js (if not already present)
RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash - \
    && apt-get install -y nodejs

# Install Rust
RUN curl https://sh.rustup.rs -sSf | sh -s -- -y

ENV PATH="/root/.cargo/bin:${PATH}"

# Install Hardhat globally
RUN npm install -g hardhat

# Optional: install Truffle
# RUN npm install -g truffle
