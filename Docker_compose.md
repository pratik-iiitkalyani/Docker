# Docker Compose
Docker compose?
- tool for defining & running multi-container docker applications
- use yaml files to configure application services (docker-compose.yml)
- can start all services with a single command : docker compose up
- can stop all services with a single command : docker compose down
- can scale up selected services when required

Step 1: install docker compose(already installed on windows and mac with docker)
check version of docker compose
```
docker-compose -v/--version
```
- on linux
method 1:
go to https://github.com/docker/compose/releases

method 2: using pip
```
pip install -U docker-compose
```

Step 2 : Create docker compose file at any location on your system
- docker-compose.yml(standard name)

step 3: Add instructions in docker-compose.yml file
- 
```
version: '<version>'
services:

    web:
        image: nginx
        # expose web serve on 8080
        ports:
        - "8080:80"
    database:
        image: redis
```
step 4: Check the validity of file by command (first go to the location where your comfig file is present)
```
docker-compose config
```
- NOTE: if that error *Version in ".\docker-compose.yml" is invalid. You might be seeing this error because you're using the wrong Compose file version. Either specify a supported version (e.g "2.2" or "3.3") and place your service definitions under the `services` key, or omit the `version` key and place your service definitions at the root of the file to use version 1.
For more on the Compose file format versions, see https://docs.docker.com/compose/compose-file/* like that go to that doc link and see which version your dockor-compose file is supporting and changed the version to that

- if you get the content of your .yml file, means it's fine and we can start running this
Step 4 : Run docker-compose.yml file
- -d says start in detached mode
```
docker-compose up -d
```
- run *docker ps* to see your container is running
Steps 5 : Bring down application
```
docker-compose down
```

How to scale services?
```
docker-compose up -d --scale database=4
```
