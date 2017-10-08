FROM docker:17.06
MAINTAINER Louis Bao <louis.bao@icloud.com>

RUN apk add --no-cache py-pip
RUN pip install docker-compose
RUN which ssh-agent || ( apk --update add openssh-client )
