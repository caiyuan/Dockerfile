#
# Debian Dockerfile
#

# Pull base image.
FROM debian:10.5

# Define ARG variables.
ARG BUSYBOX_BIN="https://busybox.net/downloads/binaries/1.31.0-defconfig-multiarch-musl/busybox-x86_64"

# Get BusyBox
ADD $BUSYBOX_BIN /tmp/

RUN \
  mv /tmp/busybox* /bin/busybox && \
  chmod +x /bin/busybox && \
  /bin/busybox --install

# Install.
RUN \
  sed -i 's/deb.debian.org/mirrors.tuna.tsinghua.edu.cn/g' /etc/apt/sources.list && \
  sed -i 's/security.debian.org/mirrors.tuna.tsinghua.edu.cn/g' /etc/apt/sources.list && \
  apt-get update && \
  apt-get -y upgrade && \
  apt-get install -y zsh && \
  rm -rf /var/lib/apt/lists/*

# Default Shell
SHELL ["/bin/zsh","-c"]

# Define default command.
CMD ["zsh"]