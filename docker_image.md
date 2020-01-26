# Docker Images
Docker Images are templates used to create Docker containers (stored in registery)
- Container is a running instance of image

list out all the images
```
docker images
```
pull the image from local or docker repo
```
docker pull <image_name>
```
pull the image from specific version
```
docker pull <image_name:version>
```
get only images id
```
docker images -q/--quiet
```
filter flag
- return all untaged images or not assocaited with any running container
```
docker images -f "dangling=flase"
```
```
docker images -f "dangling=flase"
```
- *dangling image is one that is not tagged and is not referenced by any container*

run an images(by running an image we actually create a container out of an images) 
```
docker run <image_name>
```
- *Note: if you run the container using 'docker run <image_name>' it will create a container and then run 'docker ps' will not
show the any container because container is not running
so, we have to run container*

run the container(starts the shell)-we can also run without bash
```
docker run -it <image_name> bash
```
we can also give name to the container
```
docker run --name <name> -it <image_name>
```
remove image
```
docker rmi <image_name>/<image_id>
```
inspect image
```
docker inspect <image_name>
```
