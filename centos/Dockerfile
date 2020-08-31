#
# Centos Dockerfile
#

# Pull base image.
FROM centos:8.2.2004

# Install.
RUN \
  yum -y upgrade && \
  yum install -y busybox zsh && \
  yum clean all

RUN \
  /bin/busybox --install

# Default Shell
SHELL ["/bin/zsh","-c"]

# Define default command.
CMD ["zsh"]