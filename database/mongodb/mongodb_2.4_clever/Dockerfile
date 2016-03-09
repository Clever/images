# Used in tests and in production on the mongo-docker-pipeline machines
# Published to mongo/clever:2.4
FROM ubuntu:precise
RUN apt-get -qq update && apt-get -y install wget                       && \
    wget http://fastdl.mongodb.org/linux/mongodb-linux-x86_64-2.4.0.tgz && \
    tar xzf mongodb-linux-x86_64-2.4.0.tgz                              && \
    install -t /usr/bin mongodb-linux-x86_64-2.4.0/bin/*                && \
    mkdir -p /data/db /var/lib/mongodb/                                 && \
    rm mongodb-linux-x86_64-2.4.0.tgz                                   && \
    rm -rf mongodb-linux-x86_64-2.4.0
EXPOSE 27017
ENTRYPOINT ["usr/bin/mongod"]
CMD ["--noprealloc", "--smallfiles", "--nojournal", "--replSet", "TailTest"]
