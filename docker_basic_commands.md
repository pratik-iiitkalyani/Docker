# Basic
gives the information about the Docker
```
docker version
```
docker version
```
docker -v/docker --version
```
details information about installed docker
```
docker info
```
get information about any docker commands (docker --help)
```
docker image --help
```
login to docker hub
```
docker login
```

# Images
(docker images --help - get info about all docker image command)
get list of all images
```
docker images
```
pull the images from local or docker repo
```
docker pull <image_name>
```
get only images id 
```
docker images -q/--quiet
```
get all details of all images
```
docker images -a/--all
```
remove docker image
```
docker rmi <image_id>
```
force remove docker images
```
docker rmi -f <image_id>
```
# Container

list the all running containers
```
docker ps
```
list the all the containers
```
docker ps -a
```
list of container with stats
```
docker ps -l
```
To the run the image
```
docker run <image_name>
```
To run the container in interactive mode and go inside the container
```
docker run -it <image_name>
```
run image with port
```
docker run -p <port>:<port running on container> <image_id>
```
run image as daemon
```
docker run -d <image_id>
```
- *Note: if you run the container using <docker run <image_name>> and then run > docker ps will not show the any container running 
so, we have to run container in interactive mode using docker run -it <image_name> and you will be inside the conatiner*

start the container
```
docker start <container_id>
```
stop the container
```
docker stop <container_id>
```
kill container
```
docker kill <container_id>
```
remove container
```
docker rm <container_id>
```



