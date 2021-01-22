FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get install --assume-yes \
    openjdk-11-jdk-headless \
    npm

RUN npm -v
RUN npm install sfdx-cli

ENV SFDX_CONTAINER_MODE true
ENV SHELL /bin/bash