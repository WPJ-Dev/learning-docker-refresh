FROM ubuntu:24.04

RUN apt-get update -y
# RUN apt-get install -y software-properties-common python-software-properties
# RUN add-apt-repository ppa:chris-lea/redis-server
RUN apt-get install lsb-release curl gpg -y
RUN curl -fsSL https://packages.redis.io/gpg | gpg --dearmor -o /usr/share/keyrings/redis-archive-keyring.gpg
RUN chmod 644 /usr/share/keyrings/redis-archive-keyring.gpg
RUN echo "deb [signed-by=/usr/share/keyrings/redis-archive-keyring.gpg] https://packages.redis.io/deb $(lsb_release -cs) main" | tee /etc/apt/sources.list.d/redis.list
RUN apt-get -y update
RUN apt-get -y install redis

VOLUME ["/var/log/redis"]

EXPOSE 6379
ENTRYPOINT ["redis-server"]
CMD ["--logfile", "/var/log/redis/redis-server.log"]
