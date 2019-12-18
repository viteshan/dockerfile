
# Pull base image.
FROM ubuntu:18.04

# Install.
RUN \
  sed -i 's/security\.ubuntu\.com/mirrors\.aliyun\.com/g' /etc/apt/sources.list && \
  sed -i 's/archive\.ubuntu\.com/mirrors\.aliyun\.com/g' /etc/apt/sources.list && \
  apt-get update && \
  apt-get -y upgrade && \
  apt-get install -y build-essential && \
  apt-get install -y software-properties-common && \
  apt-get install -y curl git htop man unzip vim wget inetutils-ping && \
  rm -rf /var/lib/apt/lists/*

# Add files.


# Set environment variables.
ENV HOME /root

# Define working directory.
WORKDIR /root

# Define default command.
CMD ["bash"]