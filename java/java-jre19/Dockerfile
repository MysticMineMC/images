# ----------------------------------
# MysticMineMC Java JRE19
# Image: ghcr.io/mysticminemc/images:java-jre19
# ----------------------------------

FROM        openjdk:19-slim-bullseye

LABEL       author="MysticMineMC" maintainer="support@mysticminemc.net"

RUN apt-get update -y \
 && apt-get install fontconfig iproute2 curl -y \
 && useradd -d /home/container -m container

USER container
ENV  USER=container HOME=/home/container

WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh

CMD         ["/bin/bash", "/entrypoint.sh"]