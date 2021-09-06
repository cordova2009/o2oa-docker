FROM centos:7
ENV WEB_PORT=9900\
  NODE_PORT=20010\
  APP_PORT=20020\
  CENTER_PORT=20030
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && echo 'Asia/Shanghai'
WORKDIR /data/o2server
COPY . ./
#RUN chmod 777 /data

RUN yum install -y fontconfig
#RUN yum install -y urw-fonts
EXPOSE $WEB_PORT $APP_PORT $CENTER_PORT
ENTRYPOINT /bin/sh -c "/data/o2server/start_linux.sh"