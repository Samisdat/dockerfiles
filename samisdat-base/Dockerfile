# ======================================================================= 
# An image that contain basic stuff, i need to develop:                          
# * zsh                                                              
# * git, tig git flow                                                              
# * vim
# * node
# ======================================================================= 

FROM node-9.3.0-alpine
MAINTAINER samisdat bastian@pertz.eu

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


WORKDIR /

EXPOSE 80

EXPOSE 138/udp
EXPOSE 139
EXPOSE 445
EXPOSE 445/udp

