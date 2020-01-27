# How to run jenkins on docker container
pull the jenkins image from repo
```
docker pull jenkins
```
running the docker container
- -p command is to expose the port 8080 on host system which corresponds to 8080 port for the docker server.
- similarly we are exporting 50000 for jenkins API
```
docker run -p 8080:8080 -p 50000:50000 jenkins (not recommended)
```
- Note: *if we run this command this will start jenkins server on docker container and we can access jenkins on localhost:8080
however with this command the data or jenkins home directory where all our plugins, all our jobs and all the information that we do on jenkins
will be coupled with the container and once we stop the container or delete the container all the data will also deleted. So it is not recommended
because we want Presistent storage for our jenkins home directory*

running the container and use -v for give local location for the jenkins home(recommended) - on windows
- name is optional
```
docker run --name MyJenkins -p 8080:8080 -p 50000:50000 -v C:\\Users\\ts-pratik.kumar\\Desktop\\Jenkins_Home:/var/jenkins_home jenkins
```
- access jenkins on localhost:8080 and give password. you can get password from log or Jenkins sceret folder 
- later you can change password from ->admin->configure

- Note: *if we stop the above created container and again start the container and using the same physical location to store the data
in this time the jenkins dashboard is different and ask user and password credentials and all jobs we created earlier is stiil there
*
- that why we used persistent volume -> this is useful when we want to share our data with multiple containers

**Insted of giving physical location we can also first create volume and assign to the container**
create volume
```
docker volume create <volume_name>
```
run the docker container
```
docker run --name MyJenkins -p 8080:8080 -p 50000:50000 -v <volume_name>:/var/jenkins_home jenkins
```
*after running the container we can inspect the conatiner and see assigned volume in mount key*

- other command
list the volume
```
docker volume ls
```
inspect the created volume
```
docker volume inspect <volume_name>
```

