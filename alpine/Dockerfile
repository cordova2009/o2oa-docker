FROM  adoptopenjdk/openjdk11:x86_64-alpine-jre-11.0.11_9

LABEL maintainer="stuka2009@163.com"

ENV WEB_PORT=9900\
  NODE_PORT=20010\
  APP_PORT=20020\
  CENTER_PORT=20030\
  DEBIAN_FRONTEND=noninteractive\
  TZ=Asia/Shanghai

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories\
    && apk -U upgrade --update\
    && apk --no-cache add tzdata  ttf-dejavu fontconfig\
    && ln -snf /usr/share/zoneinfo/$TZ /etc/localtime\
    && echo '$TZ' > /etc/timezone\
	&& export CGO_ENABLED=0

VOLUME /opt/o2server/config /data/o2server/config
VOLUME /opt/o2server/commons /data/o2server/commons
WORKDIR /data/o2server
COPY . ./
EXPOSE $WEB_PORT $APP_PORT $CENTER_PORT
ENTRYPOINT /bin/sh -c "./start_linux.sh"