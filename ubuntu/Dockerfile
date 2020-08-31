#
# Ubuntu Dockerfile
#

# Pull base image.
FROM ubuntu:18.04

# Install.
RUN \
  apt-get update && \
  apt-get -y upgrade && \
  apt-get install -y busybox zsh && \
  rm -rf /var/lib/apt/lists/*

RUN \
  /bin/busybox --install

# Default Shell
SHELL ["/bin/zsh","-c"]

# Define default command.
CMD ["zsh"]