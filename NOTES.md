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













