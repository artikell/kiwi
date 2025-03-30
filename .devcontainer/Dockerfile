FROM mcr.microsoft.com/devcontainers/base:ubuntu
# Install the xz-utils package
RUN apt-get update && apt-get install -y xz-utils autoconf ccache ninja-build clang

RUN wget -q https://cmake.org/files/v3.25/cmake-3.25.0.tar.gz -O /tmp/cmake-3.25.0.tar.gz \
    && mkdir -p /tmp/cmake \
    && tar -zxf /tmp/cmake-3.25.0.tar.gz -C /tmp/cmake --strip-components=1 \
    && cd /tmp/cmake \
    && ./configure \
    && make -j16 \
    && make install \
    && rm -rf /var/lib/apt/lists/* /var/cache/debconf /var/tmp/* /tmp/*
