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

#Images
(docker images --help - get info about all docker image command)
get list of all images
```
docker images
```
pull the images from local or docker repo
```
docker pull 'image_name'
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
docker rmi 'image_id'
```
force remove docker images
```
docker rmi -f 'image_id'
```




