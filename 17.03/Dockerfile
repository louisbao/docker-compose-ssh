FROM docker:17.03
MAINTAINER Louis Bao <louis.bao@icloud.com>

RUN apk add --no-cache py-pip
RUN pip install docker-compose
RUN which ssh-agent || ( apk add --no-cache openssh-client )
