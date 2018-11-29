# Dockerfile for CentOS

FROM node:8.1.2

MAINTAINER Frend "https://github.com/FrendEr"

RUN \
  yum install git \
  git --version \
  npm install -g pm2@2.6.1

RUN \
  mkdir /data \
  cd /data \
  git clone https://github.com/FrendEr/gitlab-hooks-service.git \
  cd gitlab-hooks-service \
  npm run install --production

CMD ['pm2', 'start', '/data/gitlab-hooks-service/server.js']
