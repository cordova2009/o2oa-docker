# o2oa-docker
o2oa docker containerization

Build

To build docker image:

$cd o2server

$ docker build -t o2oa .

Run

To run docker container:

$ docker run -d -p 9900:9900 -p 20020:20020 -p 20030:20030 -v /opt/o2server/config:/data/o2server/config  o2oa:latest

