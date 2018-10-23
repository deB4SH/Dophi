FROM frolvlad/alpine-mono:5.14-glibc
MAINTAINER deB4SH<github@b4sh.de>
#INSTALL REQUIRED PACKAGES
RUN apk add unzip
#PREPARE GAME DATA ENVIRONMENT
RUN mkdir -p /rimworld
WORKDIR /rimworld
COPY files/PhiServer.zip /rimworld/PhiServer.zip
RUN unzip PhiServer.zip
WORKDIR /rimworld/PhiServer
#RUN the server
RUN touch game.log && echo 'Please run the service with mono PhiServer.exe' > game.log
ENTRYPOINT ["tail","-f", "game.log"]