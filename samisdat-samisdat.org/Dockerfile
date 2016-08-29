FROM samisdat/alpine:latest
MAINTAINER Samisdat bastian.pertz@gmail.com

RUN apk update

RUN apk add python
RUN apk add make
RUN apk add g++  

RUN touch /root/.ssh/config
RUN echo "Host gitlab git.samisdat.org" > /root/.ssh/config
RUN echo "	Port 10022" > /root/.ssh/config

RUN mkdir /var/www
WORKDIR /var/www

EXPOSE 3000 80 22

