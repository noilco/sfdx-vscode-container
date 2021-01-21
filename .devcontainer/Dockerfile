FROM ubuntu:18.04

ENV DEBIAN_FRONTEND=noninteractive

RUN cat >/etc/apt/sources.list <<$'EOF ¥n \
deb http://archive.ubuntu.com/ubuntu/ bionic main universe ¥n\
deb http://archive.ubuntu.com/ubuntu/ bionic-security main universe ¥n\
deb http://archive.ubuntu.com/ubuntu/ bionic-updates main universe\
EOF'

RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y curl

RUN curl -sL https://deb.nodesource.com/setup_4.x | bash

RUN apt-get install --assume-yes \
    openjdk-11-jdk-headless \
    nodejs

RUN npm install sfdx-cli

ENV SFDX_CONTAINER_MODE true
ENV SHELL /bin/bash