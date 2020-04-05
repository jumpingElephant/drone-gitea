FROM ubuntu:latest

RUN apt update && apt upgrade -y
RUN apt install curl -y

RUN curl --silent -L https://github.com/drone/drone-cli/releases/latest/download/drone_linux_amd64.tar.gz | tar zx
RUN install -t /usr/local/bin drone

ENV DRONE_SERVER=http://drone
ENV DRONE_TOKEN=0bvE0o7L92ek43O2G1ju3KDDClHzCShZ

ENTRYPOINT bash