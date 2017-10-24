FROM debian

RUN apt-get update && apt-get dist-upgrade -y

ADD http://teamspeak.gameserver.gamed.de/ts3/releases/3.0.13.8/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2 /tmp/

RUN apt-get install bzip2 -y
RUN tar xjf /tmp/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2

EXPOSE 9987/UDP 30033 10011
CMD /teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh
