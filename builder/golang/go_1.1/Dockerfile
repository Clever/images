FROM bradrydzewski/base
WORKDIR /home/ubuntu
USER ubuntu
ADD golang.sh /etc/drone.d/
RUN wget http://go.googlecode.com/files/go1.1.2.linux-amd64.tar.gz --quiet && \
			sudo tar -C /usr/local -xzf go1.1.2.linux-amd64.tar.gz && \
			sudo chown -R ubuntu:ubuntu /usr/local/go && \
			rm go1.1.2.linux-amd64.tar.gz
RUN PATH=/usr/local/go/bin:$PATH GOPATH=/tmp/gopath /usr/local/go/bin/go get github.com/mitchellh/gox
RUN PATH=/usr/local/go/bin:$PATH /tmp/gopath/bin/gox -build-toolchain
