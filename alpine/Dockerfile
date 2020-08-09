#
# Alpine Dockerfile
#

# Pull base image.
FROM alpine:20200626

# Install.
RUN \
  echo 'https://mirrors.aliyun.com/alpine/v3.12/main/' > '/etc/apk/repositories' && \
  apk update && \
  apk add iproute2 vim bash && \
  rm -rf /var/cache/apk/*

# Add files.

# Set environment variables.
ENV HOME /root

# Define working directory.
WORKDIR /root

# Define default command.
CMD ["sh"]

