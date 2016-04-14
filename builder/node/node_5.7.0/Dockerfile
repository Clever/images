# published as clever/drone-node:5.7.0
FROM bradrydzewski/base

WORKDIR /home/ubuntu
USER ubuntu
ADD nodejs.sh /etc/drone.d/

RUN /bin/bash -c ". /home/ubuntu/nvm/nvm.sh && nvm install v5.7.0"
