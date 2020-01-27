# Dockerfile
Dockerfile?
- A text file with instructions to build image
- Automation of Docker Image Creation

Step 1: create a file named "Dockerfile"
- when we run command '*docker build*', it searches the Dockerfile. However it is not mandatory we can give our own file name

step 2: Add instructions in Dockerfile
```
# get base image - FROM <image_name>
FROM ubuntu
# give maintainer(optional) - we can also give only email
MAINTAINER pratik kumar <pratik@gmail.com>
# run command on image
RUN apt-get update
# run something on command line during container creation
CMD ["echo", 'Hello world... my first docker image']
```
- Note: *run gets excuted during building of the image and command we give inside CMD gets excuted only when you create a container out of the image*

step 3: Build dockerfile to create image
- method 1: go to Dockerfile location and run
```
docker build .
```
- method 2: run docker build with Dockerfile location
```
docker build <Dockerfile_location>
```
- method 3: we can also use -t flag for tagging our images
```
docker build -t <image_name>:Tag <directory_of_Docekrfile>
```
Step 4 : Run image to create container
run the image
```
docker run <image_id>
```
