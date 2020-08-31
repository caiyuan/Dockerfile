#
# Alpine Dockerfile
#

# Pull base image.
FROM alpine:20200626

# Install.
RUN \
  echo 'https://mirrors.aliyun.com/alpine/v3.12/main/' > '/etc/apk/repositories' && \
  apk update && \
  apk add busybox zsh && \
  rm -rf /var/cache/apk/*

RUN \
  /bin/busybox --install

# Default Shell
SHELL ["zsh","-c"]

# Define default command.
CMD ["zsh"]