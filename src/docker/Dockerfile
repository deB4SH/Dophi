FROM frolvlad/alpine-mono:5.14-glibc
MAINTAINER deB4SH<github@b4sh.de>
#INSTALL REQUIRED PACKAGES
RUN apk add unzip
#PREPARE GAME DATA ENVIRONMENT
RUN mkdir -p /rimworld
WORKDIR /rimworld
COPY files/PhiServer4.zip /rimworld/PhiServer4.zip
RUN unzip PhiServer4.zip
WORKDIR /rimworld/PhiServer4
#RUN the server
RUN touch game.log && echo 'Please run the service with mono PhiServer.exe' > game.log
ENTRYPOINT ["tail","-f", "game.log"]