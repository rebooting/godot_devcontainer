# Use the base image from the devcontainer.json file
FROM mcr.microsoft.com/devcontainers/base:bookworm

# Install dependencies
RUN apt-get update && apt-get install -y \
    wget \
    libgl1-mesa-dri \
    libdbus-1-3 \
    libx11-6 \
    libx11-dev \
    libfontconfig1 \
    libfontconfig1-dev \
    libwayland-client0 \
    libwayland-dev \
    libxcursor1 \
    libxcursor-dev \
    libxext6 \
    libxext-dev \
    libxkbcommon0 \
    libxkbcommon-dev \
    libxinerama1 \
    libxinerama-dev \
    libxrandr2 \
    libxrandr-dev \
    libxi6 \
    libxi-dev \
    mesa-utils \
    libgl1-mesa-dri \
    libgl1-mesa-glx   \
    && rm -rf /var/lib/apt/lists/*

# Set the Godot version
ENV GODOT_VERSION=4.4.1-stable

# Download and install the full Godot binary
# https://github.com/godotengine/godot/releases/download/4.4.1-stable/Godot_v4.4.1-stable_linux.x86_64.zip
RUN wget https://github.com/godotengine/godot/releases/download/${GODOT_VERSION}/Godot_v${GODOT_VERSION}_linux.x86_64.zip -O godot.zip \
    && unzip godot.zip -d /usr/local/bin/ \
    && rm godot.zip

# Add Godot to PATH
ENV PATH="/usr/local/bin:$PATH"