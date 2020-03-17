FROM node:12-alpine

MAINTAINER "Jeremy CURNY" <jeremy.curny.pro@gmail.com>

ARG DEBIAN_FRONTEND=noninteractive

RUN \
  apk add --no-cache --quiet bash curl git openssh-client

RUN \
  mkdir -p ~/.ssh \
  && chmod 700 ~/.ssh \
  && echo "" > ~/.ssh/known_hosts \
  && echo "Host *\n  StrictHostKeyChecking no\n  UserKnownHostsFile=/dev/null\n  LogLevel ERROR" > ~/.ssh/config

RUN \
  npm install -g --silent serverless@1.60.5
