FROM frolvlad/alpine-mono:5.14-glibc
MAINTAINER deB4SH<github@b4sh.de>
#CHANGE TO ROOT USER
USER root
#INSTALL REQUIRED PACKAGES
RUN apk add unzip
#PREPARE GAME DATA ENVIRONMENT
RUN mkdir -p /rimworld
WORKDIR /rimworld
COPY files/PhiServer.zip /rimworld/PhiServer.zip
RUN unzip PhiServer4.zip
WORKDIR /rimworld/PhiServer4
#RUN the server
RUN mono PhiServer.exe > game.log
CMD ["tail", "-f", "game.log"]