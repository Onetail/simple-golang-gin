
FROM golang:1-stretch

RUN apt-get update && apt-get -y install netcat && apt-get clean

WORKDIR /app

COPY . /app/
COPY ./docker/entrypoint.sh /

RUN [ "chmod", "+x", "/entrypoint.sh"]
RUN [ "go", "build" ]

EXPOSE 3000