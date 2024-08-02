FROM ubuntu:latest

## Install sudo if it isn't installed already
RUN \
    apt-get update && apt-get install -y sudo 

## run as root user to avoid permission issues
USER root


## Install updates and upgrades and nginx
RUN \
    apt update && \
    apt upgrade -y && \
    apt install -y nginx
   
    
EXPOSE 80

CMD [ "nginx", "-g", "daemon off;" ]