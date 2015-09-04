FROM bradrydzewski/virtualenv
WORKDIR /home/ubuntu
USER ubuntu
ADD python.sh /etc/drone.d/

# install python 3.4
RUN sudo apt-get update && sudo apt-get install python3.4 python3.4-dev
RUN sudo pip install --upgrade virtualenv

# setup default virtualenv for python 3.4
RUN virtualenv --python=/usr/bin/python3.4 /home/ubuntu/virtualenv/python3.4 --system-site-packages && \
		. /home/ubuntu/virtualenv/python3.4/bin/activate && \
		pip install --use-mirrors nose && \
		pip install -U pytest
