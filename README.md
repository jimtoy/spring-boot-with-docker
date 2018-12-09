# Spring Boot with Docker

A worked example following https://spring.io/guides/gs/spring-boot-docker/

## Commands
mvn install dockerfile:build
docker run --name jimtoy-docker -p 8080:8080 -t jimtoy/gs-spring-boot-docker 

docker stop jimtoy-docker
docker rm jimtoy-docker

## Issues