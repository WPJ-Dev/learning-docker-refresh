FROM ubuntu:25.10

RUN apt-get update -y;
RUN apt-get install curl -y;
RUN curl -fsSL https://deb.nodesource.com/setup_24.x | bash -;
RUN apt-get install -y nodejs;

COPY index.js /app/index.js
WORKDIR /app
CMD ["node", "index.js"]