FROM mcr.microsoft.com/devcontainers/base:ubuntu

ARG USERNAME=vscode
ARG USER_UID=1000
ARG USER_GID=$USER_UID
WORKDIR /home/developer

# Apt
RUN apt-get update
RUN apt-get install -y \
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
RUN mkdir -p /home/developer/Android/sdk/
ENV ANDROID_SDK_ROOT /home/developer/Android/sdk/
RUN mkdir -p .android
RUN touch .android/repositories.config
RUN wget -O sdk-tools.zip https://dl.google.com/android/repository/sdk-tools-linux-4333796.zip
RUN unzip sdk-tools.zip && rm sdk-tools.zip
RUN mv tools Android/sdk/tools
RUN cd Android/sdk/tools/bin
RUN yes | ./sdkmanager --licenses
RUN cd Android/sdk/tools/bin && ./sdkmanager "build-tools;29.0.2" "patcher;v4" "platform-tools" "platforms;android-29" "sources;android-29"
ENV PATH "$PATH:/home/developer/Android/sdk/platform-tools"

# Download the flutter SDK
RUN git clone https://github.com/flutter/flutter.git /home/developer/flutter/
ENV PATH "$PATH:/home/developer/flutter/bin"

#Maybe run flutter doctor and flutter -d web-application
