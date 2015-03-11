FROM bradrydzewski/base
WORKDIR /home/ubuntu
USER ubuntu
ADD golang.sh /etc/drone.d/
RUN wget http://golang.org/dl/go1.4.linux-amd64.tar.gz --quiet && \
			sudo tar -C /usr/local -xzf go1.4.linux-amd64.tar.gz && \
			sudo chown -R ubuntu:ubuntu /usr/local/go && \
			rm go1.4.linux-amd64.tar.gz
