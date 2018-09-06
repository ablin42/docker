##From a debian image you will add the appropriate sources to create a TeamSpeak
##server, that will launch along with your container. It will be deemed valid if at least
##one user can connect to it and engage in a normal discussion (no far-fetched setup), so
##be sure to create your Dockerfile with the right options. Your program should get the
##sources when it builds, they cannot be in your repository.

FROM debian:latest

EXPOSE 9987/udp 30033 10011

RUN apt-get update -y && apt-get upgrade -y && apt-get install wget -y && \
wget http://dl.4players.de/ts/releases/3.0.11.1/teamspeak3-server_linux-amd64-3.0.11.1.tar.gz && tar xvfz teamspeak3-server_linux-amd64-3.0.11.1.tar.gz

CMD ["sh", "teamspeak3-server_linux-amd64/ts3server_minimal_runscript.sh"]
