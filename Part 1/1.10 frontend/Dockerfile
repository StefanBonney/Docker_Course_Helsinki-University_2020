FROM ubuntu:18.04

WORKDIR /mydir

RUN apt-get update && apt-get install -y curl 


RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get update && apt-get install -y git && apt-get install -y nodejs

RUN git clone https://github.com/docker-hy/frontend-example-docker

RUN mv ./frontend-example-docker/* .

RUN ls && npm install

EXPOSE 5000

CMD ["npm", "start"]
