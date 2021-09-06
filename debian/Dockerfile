FROM debian:10

ENV WEB_PORT=9900\
  NODE_PORT=20010\
  APP_PORT=20020\
  CENTER_PORT=20030\
  DEBIAN_FRONTEND=noninteractive
VOLUME /opt/o2server/config /data/o2server/config

WORKDIR /data/o2server
COPY . ./
RUN apt-get update && apt-get install -y --no-install-recommends fonts-urw-base35 &&\
  apt-get install -y --no-install-recommends fontconfig
EXPOSE $WEB_PORT $APP_PORT $CENTER_PORT
ENTRYPOINT /bin/sh -c "/data/o2server/start_linux.sh"