FROM alpine:3.4
MAINTAINER Samisdat bastian.pertz@gmail.com

RUN apk update

RUN apk add htop
RUN apk add vim

#RUN apt-get install -y wget
RUN apk add curl
#RUN apt-get install -y unzip

RUN apk add git
#RUN apt-get install -y git-flow
RUN apk add tig

#install node, grunt and bower
RUN apk add nodejs
RUN npm install -g grunt-cli
RUN npm install -g bower

## install oh-my-zsh
RUN apk add zsh
ADD zsh-install.sh /zsh-install.sh
RUN chmod +x zsh-install.sh
RUN echo "hallo"
RUN ./zsh-install.sh
RUN rm zsh-install.sh

## install ssh-server; used to mount via ssh
RUN apk add openssh
RUN mkdir /var/run/sshd
RUN sed -i 's@#PasswordAuthentication yes@PasswordAuthentication no@g' /etc/ssh/sshd_config
RUN mkdir /root/.ssh

WORKDIR /

EXPOSE 80 22

