# ======================================================================= 
# An image that contain basic stuff, i need to develop:                          
# * zsh                                                              
# * git, tig git flow                                                              
# * vim
# * node
# ======================================================================= 

FROM node:9.3.0-alpine
MAINTAINER samisdat bastian@pertz.eu

RUN apk update

# ======================================================================= 
RUN apk add htop
RUN apk add vim
RUN apk add wget
RUN apk add curl

# ======================================================================= 

RUN apk add git
RUN apk add tig

# ======================================================================= 
RUN apk add zsh
ADD zsh-install.sh /zsh-install.sh
RUN chmod +x zsh-install.sh
RUN ./zsh-install.sh
RUN rm zsh-install.sh

WORKDIR /

EXPOSE 80

