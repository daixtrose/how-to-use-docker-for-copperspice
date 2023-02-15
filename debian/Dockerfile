ARG VERSION
FROM debian:$VERSION

LABEL maintainer="Markus Werle <daixtrose@users.noreply.github.com>"

# Install basic build dependencies
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    lsb-release \
    pkg-config \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Install some build tool helper
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    ccache \
    ninja-build \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Install emulation tools
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    qemu \
    binfmt-support \
    qemu-user-static \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Add "armhf" architecture to Debian multiarch configuration
RUN dpkg --add-architecture armhf
RUN dpkg --add-architecture aarch64 

CMD ["/bin/bash"]
