FROM debian:bookworm

ENV DEBIAN_FRONTEND=noninteractive

# Update repos + upgrade system
RUN apt-get update && apt-get -y full-upgrade

# Install package dependencies
RUN apt-get install -y \
    clang \
    cmake \
    curl \
    git \
    qt6-base-dev \
    qt6-l10n-tools \
    qt6-multimedia-dev \
    qt6-tools-dev \
    qt6-tools-dev-tools \
    libxext-dev

# Download Transifex client
RUN curl -o- https://raw.githubusercontent.com/transifex/cli/master/install.sh | bash
RUN mv /tx /usr/bin/
