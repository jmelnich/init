FROM debian
LABEL maintainer="imelnych"
RUN apt-get update -y

#DEPENDENCIES
RUN	apt-get install -y wget p7zip-full \
&& wget http://dl.4players.de/ts/releases/3.0.12.3/teamspeak3-server_linux_amd64-3.0.12.3.tar.bz2 \
&&  7z x teamspeak3-server_linux_amd64-3.0.12.3.tar.bz2 \
&& tar xf teamspeak3-server_linux_amd64-3.0.12.3.tar

ENTRYPOINT teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh

###### CHECK ######
# lets run in interactive mode because we need token
# docker run --rm -it -p 9987:9987/udp my-teamspeak
# go to connections => connect in teamspeak client app and set address to (docker-machine ip Char):9987 and set given token
