# Containers
What are Containers?
Containers are running instances of Docker Images

list the all running containers
```
docker ps
```
list all the containers
```
docker ps -a
```
create container from image
```
docker run <image_name>
```
- Note: *it will create a container, not start the container*
start the container in interactive mode
```
docker run --name <name> -it <image_name>
```
start the container
```
docker start <container_id | container_name>
```
stop the container
```
docker stop <container_id | container_name>
```
pause the container(after pausing the container, bash will stop working)
```
docker pause <container_id | container_name>
```
resume the container
```
docker unpause <container_id | container_name>
```
Show top process of container
```
docker top <container_id | container_name>
```
show stats of running container
```
docker stats <container_id | container_name>
```
go inside the container
```
docker exec -it <container_id | container_name> bin/bash
```
get ip address of container
```
docker inspect <container_id> | grep IPAddress
```
attach to your running container
```
docker attach <container_id | container_name>
```
kill container
```
docker kill <container_id | container_name>
```
remove container
```
docker rm <container_id | container_name>
```
get history of the image
```
docker history <image_id | image_name>
