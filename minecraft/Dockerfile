FROM debian:latest

ENV JDK_VERSION 7

RUN apt-get update
RUN apt-get install -y openjdk-$JDK_VERSION-jdk

ENV JAVA_HOME /usr/lib/jvm/java-$JDK_VERSION-openjdk-amd64
ENV PATH $PATH:$JAVA_HOME/bin

RUN groupadd -g 500 minecraft
RUN useradd -m -s /bin/bash minecraft -u 500 -g 500

USER minecraft
ENTRYPOINT /home/minecraft/server/run
