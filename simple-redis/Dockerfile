FROM ubuntu:14.04
RUN apt-get update
RUN apt-get -y install redis-server redis-tools
EXPOSE 4567
ENTRYPOINT [ "/usr/bin/redis-server" ]

