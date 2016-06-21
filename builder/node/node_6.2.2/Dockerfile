# published as clever/drone-node:6.2.2
FROM bradrydzewski/base

WORKDIR /home/ubuntu
USER ubuntu
ADD nodejs.sh /etc/drone.d/

RUN /bin/bash -c ". /home/ubuntu/nvm/nvm.sh && nvm install v6.2.2"
