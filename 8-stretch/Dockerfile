FROM node:8-stretch

MAINTAINER "Jeremy CURNY" <jeremy.curny.pro@gmail.com>

ARG DEBIAN_FRONTEND=noninteractive

RUN  \
    apt-get update \
    && apt-get install -y git jq rsync sshpass unzip zip \
    && apt-get clean autoclean \
    && apt-get autoremove

RUN \
    mkdir -p ~/eslint/standard ~/eslint/semistandard \
    && npm install -g eslint jshint jslint semistandard standard \
    && npm install -g eslint-plugin-import eslint-plugin-node eslint-plugin-promise eslint-plugin-standard \
    && npm install -g eslint-config-standard eslint-config-semistandard \
    && echo '{"extends": ["standard"]}' > ~/eslint/standard/.eslintrc.json \
    && echo '{"extends": ["semistandard"]}' > ~/eslint/semistandard/.eslintrc.json \
    && npm install -g bower gulp grunt mocha \
    && npm install -g serverless serverless-domain-manager

RUN \
    mkdir -p ~/.ssh \
    && chmod 700 ~/.ssh \
    && echo "" > ~/.ssh/known_hosts
