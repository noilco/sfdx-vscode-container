FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get install -y \
    openjdk-11-jdk-headless \
    npm \
    git

RUN npm -v
RUN npm install sfdx-cli --global --unsafe-perm
RUN sfdx --version

ENV SFDX_CONTAINER_MODE true
ENV SHELL /bin/bash