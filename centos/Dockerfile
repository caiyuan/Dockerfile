#
# Centos Dockerfile
#

# Pull base image.
FROM centos:8.2.2004

# Define ARG variables.
ARG BUSYBOX_BIN="https://busybox.net/downloads/binaries/1.31.0-defconfig-multiarch-musl/busybox-x86_64"

# Install.
RUN \
  yum -y upgrade && \
  yum install -y wget zsh && \
  wget -O /root/busybox $BUSYBOX_BIN && chmod +x /root/busybox && mv /root/busybox /bin/busybox && \
  yum clean all

RUN \
  /bin/busybox --install

# Default Shell
SHELL ["/bin/zsh","-c"]

# Define default command.
CMD ["zsh"]