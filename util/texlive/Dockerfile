FROM debian:jessie
MAINTAINER nate.brennand@clever.com
# Install latex related tooling:
RUN apt-get update -y && \
    apt-get install ca-certificates -y && \
    apt-get -y install wget build-essential && \
    apt-get -y install texlive-full
