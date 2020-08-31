#
# Centos Dockerfile
#

# Pull base image.
FROM centos:8.2.2004

# Define ARG variables.
ARG BUSYBOX_BIN="https://busybox.net/downloads/binaries/1.31.0-defconfig-multiarch-musl/busybox-x86_64"

# Get BusyBox
ADD $BUSYBOX_BIN ~

RUN \
  mv ~/busybox* /bin/busybox && \
  chmod +x /bin/busybox && \
  /bin/busybox --install

# Install.
RUN \
  yum -y upgrade && \
  yum install -y zsh && \
  yum clean all

# Default Shell
SHELL ["/bin/zsh","-c"]

# Define default command.
CMD ["zsh"]