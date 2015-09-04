FROM bradrydzewski/base
WORKDIR /home/ubuntu
USER ubuntu
ADD golang.sh /etc/drone.d/
RUN wget https://storage.googleapis.com/golang/go1.5.linux-amd64.tar.gz --quiet && \
			sudo tar -C /usr/local -xzf go1.5.linux-amd64.tar.gz && \
			sudo chown -R ubuntu:ubuntu /usr/local/go && \
			rm go1.5.linux-amd64.tar.gz
