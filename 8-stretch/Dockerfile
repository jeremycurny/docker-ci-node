FROM node:8-stretch

MAINTAINER "Jeremy CURNY" <jeremy.curny.pro@gmail.com>

ARG DEBIAN_FRONTEND=noninteractive

RUN  \
    apt-get update \
    && apt-get install -y git sshpass \
    && apt-get clean autoclean \
    && apt-get autoremove

RUN \
    npm install -g bower \
    && npm install -g gulp \
    && npm install -g grunt

RUN \
    mkdir -p /root/.ssh \
    && chmod 700 /root/.ssh \
    && echo "" > /root/.ssh/known_hosts
