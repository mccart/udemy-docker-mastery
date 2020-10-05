# Udemy Course Docker Mastery: with Kubernetes+Swarm from a Docker Captain

> Build, test, deploy containers with the best mega-course on Docker, Kubernetes, Compose, Swarm and Registry using DevOps

This repo is for use in my Udemy Courses "Docker Mastery" and "Swarm Mastery"

NOTE: As of July 2020 the new default branch is `main`, so please update your clone if you're still on `master` branch.

Get these courses for with my "cheapest on the Internet" coupon links:

https://www.bretfisher.com/courses

My other DevOps and Docker resources are at https://www.bretfisher.com/docker

Feel free to create issues or PRs if you find a problem with examples in this repo!

------------------------

docker version
docker info
docker

# images vs container

docker container run --publish 80:80 nginx
docker container run --publish 80:80 --detach nginx
docker container ls
docker container stop <id>
docker container ls
docker container ls -a

docker container run --publish 80:80 --detach --name webhost nginx
docker container ls -a
docker container logs webhost <options>
docker container top webhost
docker container --help

docker container ls -a
docker container rm <id> <id> ... # rm stopped containers
docker container rm -f <id> ...   # force rm running containers

docker run --name mongo -d mongo
docker ps
docker top mongo
docker desktop -> mongo container -> cli -> ps aux
docker stop mongo
docker start mongo
docker stop mongo
docker rm mongo

assignment: manage multiple containers

dock container run -p 80:80 -d --name proxy nginx
dock container run -p 8080:80 -d --name webserver httpd
dock container run -p 3306:3306 -d -e MYSQL_RANDOM_ROOT_PASSWORD=yes --name db mysql
docker container logs mysql
docker container logs nginx
docker container logs httpd

curl localhost
curl localhost:8080

docker container ps
docker container ps -a
docker container stop ..ids..
docker container rm ..ids..
docker container ls
docker container ls -a

docker container top
docker container inspect
docker container stats

docker container run -it  // run interactively

// start debian 10 buster container, shell into bash
docker container run -it --name proxy nginx bash
# cat /etc/os-release

// start ubuntu 20.04.1 container, shell into bash
docker container run -it --name ubuntu ubuntu
# cat /etc/os-release
# apt-get update
# apt-get install curl
# curl google.com
# exit  // stops container

// start stopped container, shell into bash (default)
docker container start -ai ubuntu
# curl google.com

// attach to running container, shell into bash
docker container exec -it mysql bash
# apt-get update
# apt-get install -y procps
# ps aux
# exit

docker pull alpine
docker image ls
// apline 3.12.0, uses apk package manager
docker container run -it alpine sh
# apk fetch coffee

docker container run -p
docker containter port <container>

docker container run -p 80:80 --name webhost nginx -d nginx
docker container port webhost
80/tcp -> 0.0.0.0:80

docker container inspect --format "{{ .NetworkSettings.IPAddress }}" webhost
ifconfig eth0


docker network ls
docker network inspect
docker network create --driver
docker network connect
docker network disconnect

