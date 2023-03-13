# ----------------------------------
# MysticMineMC Java Azul  Prime 19
# Image: ghcr.io/mysticminemc/images:azul-prime-19
# ----------------------------------

FROM        azul/prime:19

LABEL       author="MysticMineMC" maintainer="support@mysticminemc.net"

RUN apt-get update -y \
 && apt-get install fontconfig iproute2 curl -y \
 && useradd -d /home/container -m container

USER container
ENV  USER=container HOME=/home/container

WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh

CMD         ["/bin/bash", "/entrypoint.sh"]
