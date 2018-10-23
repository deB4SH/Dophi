FROM debian:buster-slim
#update sources
RUN apt-get update
#install packages
RUN apt-get install mono-complete mono-runtime mono-dmcs tzdata wget unzip -y
#clean up container
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /var/tmp/*
#================
#GAME RELATED STEPS
#================
#PREPARE GAME DATA ENVIRONMENT
RUN mkdir -p /rimworld
WORKDIR /rimworld
COPY files/PhiServer.zip /rimworld/PhiServer.zip
RUN unzip PhiServer.zip
WORKDIR /rimworld/PhiServer
#RUN the server
RUN mono PhiServer.exe > game.log
CMD ["tail", "-f", "game.log"]