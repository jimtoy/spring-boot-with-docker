# Spring Boot with Docker

A worked example following https://spring.io/guides/gs/spring-boot-docker/

## Commands
mvn install dockerfile:build
docker run --name jimtoy-docker -p 8080:8080 -t jimtoy/gs-spring-boot-docker 

docker stop jimtoy-docker
docker rm jimtoy-docker

## Issues


## Run on AWS
https://docs.aws.amazon.com/AmazonECS/latest/developerguide/docker-basics.html
sudo yum update -y
sudo amazon-linux-extras install docker
sudo service docker start
sudo usermod -a -G docker ec2-user

docker run --name jimtoy-docker -p 80:8080 -t jimtoy/gs-spring-boot-docker 

### Manager 1
docker swarm init --advertise-addr 1.1.1.1  --listen-addr 1.1.1.1


## Join Manager
docker swarm join-token manager 

docker node ls

## Join Worker
docker swarm join-token worker


docker service create --name jimtoy-docker -p 80:8080 --replicas 4 jimtoy/gs-spring-boot-docker