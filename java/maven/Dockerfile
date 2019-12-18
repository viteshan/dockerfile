FROM viteshan/oraclejava:8

MAINTAINER viteshan <viteshan@163.com>

# Default to UTF-8 file.encoding
ENV LANG en_US.UTF-8


# Download the Maven from
#
#  https://maven.apache.org/download.cgi
#	
# and place it on the same directory as the Dockerfile
#

ARG MAVEN_PKG=apache-maven-3.6.3-bin.tar.gz 


COPY $MAVEN_PKG /tmp/apache-maven.tar.gz


RUN set -eux; mkdir -p /usr/share/maven; \
  tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1;\
  rm /tmp/apache-maven.tar.gz;\
  ln -s /usr/share/maven/bin/mvn /usr/bin/mvn;

ENV MAVEN_HOME /usr/share/maven