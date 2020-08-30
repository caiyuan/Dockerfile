#
# Debian Dockerfile
#

# Pull base image.
FROM debian:10.5

# Install.
RUN \
  sed -i 's/deb.debian.org/mirrors.tuna.tsinghua.edu.cn/g' /etc/apt/sources.list && \
  sed -i 's/security.debian.org/mirrors.tuna.tsinghua.edu.cn/g' /etc/apt/sources.list && \
  apt-get update && \
  apt-get -y upgrade && \
  apt-get install -y busybox && \
  rm -rf /var/lib/apt/lists/*

RUN \
  ln -s /bin/busybox /bin/top && \
  ln -s /bin/busybox /bin/ps && \
  ln -s /bin/busybox /bin/sysctl && \
  ln -s /bin/busybox /bin/ifconfig && \
  ln -s /bin/busybox /bin/route && \
  ln -s /bin/busybox /bin/brctl && \
  ln -s /bin/busybox /bin/arp && \
  ln -s /bin/busybox /bin/netstat && \
  ln -s /bin/busybox /bin/wget && \
  ln -s /bin/busybox /bin/vi

# Set environment variables.
ENV HOME /root

# Define working directory.
WORKDIR /root

# Define default command.
CMD ["bash"]
