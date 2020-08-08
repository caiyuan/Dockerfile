#
# Centos Dockerfile
#

# Pull base image.
FROM centos:8.2.2004

# Install.
RUN \
  yum -y upgrade && \
  yum install -y iproute vim && \
  yum clean all

# Add files.

# Set environment variables.
ENV HOME /root

# Define working directory.
WORKDIR /root

# Define default command.
CMD ["bash"]

