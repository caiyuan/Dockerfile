#
# Docker-zsh Dockerfile
#

# Pull base image.
FROM docker:19.03.12-git

# Install.
RUN \
  echo 'https://mirrors.aliyun.com/alpine/v3.12/main/' > '/etc/apk/repositories' && \
  apk update && \
  apk add zsh && \
  rm -rf /var/cache/apk/*

RUN \
  sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)" && \
  sed -i 's/"robbyrussell"/"dieter"/g' ~/.zshrc

# Default Shell
SHELL ["/bin/zsh","-c"]

# Define default command.
CMD ["zsh"]
