# o2oa-docker
o2oa docker containerization

## Build

To build docker image:
```Docker
cd o2server
docker build -t o2oa .
```


## Run

To run docker container:
```Docker
$ docker run -d -p 9900:9900 -p 20020:20020 -p 20030:20030 -v /opt/o2server/config:/data/o2server/config  o2oa:latest
```


Of course, you can write your own compose to run the docker container.


