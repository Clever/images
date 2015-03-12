FROM bradrydzewski/virtualenv
WORKDIR /home/ubuntu
USER ubuntu
ADD python.sh /etc/drone.d/

RUN sudo add-apt-repository --yes ppa:pypy/ppa

# install all python
RUN sudo apt-get update                             && \
    sudo apt-get install python2.6 python2.6-dev    && \
    sudo apt-get install python2.7 python2.7-dev    && \
    sudo apt-get install python3.1 python3.1-dev    && \
    sudo apt-get install python3.2 python3.2-dev    && \
    sudo apt-get install python3.3 python3.3-dev    && \
    sudo apt-get install python3.4a python3.4-dev   && \
    sudo apt-get install pypy pypy-dev

# setup default virtualenv
RUN virtualenv /home/ubuntu/virtualenv --system-site-packages && \
		. /home/ubuntu/virtualenv/bin/activate && \
		pip install --use-mirrors tox && \
		pip install --use-mirrors nose && \
		pip install -U pytest
