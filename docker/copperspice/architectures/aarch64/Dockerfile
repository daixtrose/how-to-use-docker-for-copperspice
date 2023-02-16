ARG VERSION

FROM debian:$VERSION

LABEL maintainer="Markus Werle <daixtrose@users.noreply.github.com>"

RUN apt-get update \
 && apt-get install -y --no-install-recommends \
    git=$VERSION \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*


# Fetch updated package list
RUN apt-get update && apt-get install -y

# Install basic build dependencies
RUN apt-get install -y \
  cmake \
  g++ \
  git \
  lsb-release \
  pkg-config \
  ccache \
  ninja-build

# Install host CS build dependencies
RUN apt-get install -y \
  libfreetype6-dev \
  libasound2-dev \
  libaudio-dev \
  libc6-dev \
  libfontconfig1-dev \
  libgl1-mesa-dev \
  libglib2.0-dev \
  libgstreamer-plugins-base1.0-dev \
  libgstreamer1.0-dev \
  libice-dev \
  libpulse-dev \
  libsm-dev \
  libx11-dev \
  libx11-xcb-dev \
  libxcb-icccm4-dev \
  libxcb-image0-dev \
  libxcb-keysyms1-dev \
  libxcb-randr0-dev \
  libxcb-render-util0-dev \
  libxcb-render0-dev \
  libxcb-shape0-dev \
  libxcb-shm0-dev \
  libxcb-sync-dev \
  libxcb-xfixes0-dev \
  libxcb-xinerama0-dev \
  libxcb-xkb-dev \
  libxcb1-dev \
  libxcursor-dev \
  libxext-dev \
  libxfixes-dev \
  libxi-dev \
  libxinerama-dev \
  libxkbcommon-dev \
  libxkbcommon-x11-dev \
  libxml2-dev \
  libxrandr-dev \
  libxrender-dev \
  libxt6 \  
  libxcb-glx0-dev \
  libcups2-dev

# Install emulation tools
RUN apt-get install -y \
  qemu \
  binfmt-support \
  qemu-user-static 

# Add "aarch64" architecture to Debian multiarch configuration
RUN dpkg --add-architecture aarch64
RUN apt-get update

# Install cross compiler
RUN apt-get install -y \
  gcc-10-arm-linux-gnueabihf \
  g++-10-arm-linux-gnueabihf

# Install target CS build dependencies
RUN apt-get install -y \
  libatomic1:aarch64 \
  libice-dev:aarch64 \
  libsm-dev:aarch64 \
  libx11-dev:aarch64 \
  libx11-xcb-dev:aarch64 \
  libxcursor-dev:aarch64 \
  libxext-dev:aarch64 \
  libxfixes-dev:aarch64 \
  libxi-dev:aarch64 \
  libxinerama-dev:aarch64 \
  libxkbcommon-dev:aarch64 \
  libxkbcommon-x11-dev:aarch64 \
  libxml2-dev:aarch64 \
  libxrandr-dev:aarch64 \
  libxrender-dev:aarch64 \
  libxcb-icccm4-dev:aarch64 \
  libxcb-image0-dev:aarch64 \
  libxcb-keysyms1-dev:aarch64 \
  libxcb-randr0-dev:aarch64 \
  libxcb-render-util0-dev:aarch64 \
  libxcb-render0-dev:aarch64 \
  libxcb-shape0-dev:aarch64 \
  libxcb-shm0-dev:aarch64 \
  libxcb-sync-dev:aarch64 \
  libxcb-xfixes0-dev:aarch64 \
  libxcb-xinerama0-dev:aarch64 \
  libxcb-xkb-dev:aarch64 \
  libgl1-mesa-dev:aarch64 \
  libfontconfig1-dev:aarch64 \
  libxcb-glx0-dev:aarch64 \
  libgstreamer-plugins-base1.0-dev:aarch64 \
  libgstreamer1.0-dev:aarch64 \
  libaudio-dev:aarch64 \
  libpulse-dev:aarch64

# Executable to verify ARM binary emulation is operating
RUN apt-get install -y hello:aarch64
