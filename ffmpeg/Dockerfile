##docker build -t yankchina/ffmpeg:1.0 .
FROM jrottenberg/ffmpeg:3.3-ubuntu

LABEL maintainer="yankchina@gmail.com"
LABEL version="1.0"

ENTRYPOINT []

WORKDIR /home

#install node.js & pm2
##[https://stackoverflow.com/questions/25899912/how-to-install-nvm-in-docker/60137919#60137919]
SHELL ["/bin/bash", "--login", "-i", "-c"]
RUN apt update && apt install -y curl
RUN curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
RUN source ~/.profile
RUN source /root/.bashrc && nvm install node
RUN npm install pm2 -g
RUN apt clean
SHELL ["/bin/bash", "--login", "-c"]

EXPOSE 8080