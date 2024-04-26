FROM mcr.microsoft.com/devcontainers/base:ubuntu

ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID

# Install necessary packages
RUN apt-get update && \
    apt-get install -y \
    curl \
    git \
    unzip \
    xz-utils \
    zip \
    libglu1-mesa \
    openjdk-8-jdk \
    wget \
    clang \
    cmake \
    ninja-build \
    pkg-config \
    libgtk-3-dev \
    liblzma-dev \
    libstdc++-12-dev

# Set up the Android SDK
RUN mkdir -p /home/developer/Android/sdk && \
    mkdir -p /home/developer/.android && \
    touch /home/developer/.android/repositories.config && \
    wget -O sdk-tools.zip https://dl.google.com/android/repository/sdk-tools-linux-4333796.zip && \
    unzip sdk-tools.zip -d /home/developer/Android/sdk && \
    rm sdk-tools.zip && \
    chown -R $USER_UID:$USER_GID /home/developer/Android

ENV ANDROID_SDK_ROOT /home/developer/Android/sdk

# Accept Android SDK licenses
RUN mkdir -p "$ANDROID_SDK_ROOT/licenses" && \
    echo "8933bad161af4178b1185d1a37fbf41ea5269c55" > "$ANDROID_SDK_ROOT/licenses/android-sdk-license" && \
    yes | $ANDROID_SDK_ROOT/tools/bin/sdkmanager --licenses

# Install additional Android SDK components
RUN $ANDROID_SDK_ROOT/tools/bin/sdkmanager "build-tools;29.0.2" "patcher;v4" "platform-tools" "platforms;android-29" "sources;android-29" || echo "Command failed"
RUN $ANDROID_SDK_ROOT/tools/bin/sdkmanager --install "cmdline-tools;latest"

ENV PATH "$PATH:$ANDROID_SDK_ROOT/platform-tools"

# Download and install Flutter SDK
RUN wget -O flutter.tar.xz https://storage.googleapis.com/flutter_infra_release/releases/beta/linux/flutter_linux_3.22.0-0.3.pre-beta.tar.xz && \
    tar xf flutter.tar.xz -C /home/developer && \
    chown -R $USER_UID:$USER_GID /home/developer/flutter && \
    rm flutter.tar.xz

# Add Flutter binary to PATH
ENV PATH "$PATH:/home/developer/flutter/bin"

# Set up non-root privilege
USER $USERNAME
