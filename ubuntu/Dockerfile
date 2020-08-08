#
# Ubuntu Dockerfile
#

# Pull base image.
FROM ubuntu:18.04

# Install.
RUN \
  apt-get update && \
  apt-get -y upgrade && \
  apt-get install -y iproute2 vim && \
  rm -rf /var/lib/apt/lists/*

# Add files.

# Set environment variables.
ENV HOME /root

# Define working directory.
WORKDIR /root

# Define default command.
CMD ["bash"]

