
1. how to search a docker image in hub.docker.com
```sh
docker search httpd
```
2. Download a docker image from hub.docker.com
```sh
docker image pull <image_name>:<image_version/tag>
```

3. List out docker images from your local system
```sh
docker image ls
```

4. Create/run/start a docker container from image
```sh
docker run -d --name <container_Name> <image_name>:<image_version/tag>

d - run your container in back ground (detached)
```

5. Expose your application to host server
```sh
docker run -d  -p <host_port>:<container_port> --name <container_Name> <image_name>:<Image_version/tag>

docker run -d --name httpd_server -p 8080:80 httpd:2.2
```

6. List out running containers
```sh
docker ps
```

7. List out all docker container (running, stpooed, terminated, etc...)
```sh
docker ps -a
```

8. run a OS based container which interactive mode (nothing but login to container after it is up and running)

```sh
docker run -i -t --name centos_server centos:latest
i - interactive
t - Terminal
```

9. Stop a container 
```sh
docker stop <container_id>
```

10. Start a container which is in stopped or exit state

```sh
docker start <container_id>
```
11. Remove a container

```sh
docker rm <container_id>
```

12. login to a docker container
```sh
docker exec -it <container_Name> /bin/bash
```

13. Latest Tomcat Image Issue -
   Usually default apps are available in "webapps" folder. But not present in latest image of Tomcat. So for fix this you have to login     in docker container and copy files with the help of below commands-:
```sh
docker exec -it <container_Name> /bin/bash- login by this command

[dockeradmin ~]$ docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS                    NAMES
c85b1e526263515        devops-project      "catalina.sh run"   5 minutes ago       Up 5 minutes        0.0.0.0:8080->8080/tcp   devops-container
[dockeradmin]$ docker exec -it devops-container /bin/bash
root@c:/usr/local/tomcat# ls
BUILDING.txt     LICENSE  README.md      RUNNING.txt  conf     lib   native-jni-lib  webapps       work
CONTRIBUTING.md  NOTICE   RELEASE-NOTES  bin          include  logs  temp            webapps.dist
root@:/usr/local/tomcat# cd webapps
root@:/usr/local/tomcat/webapps# ls
root@:/usr/local/tomcat/webapps# cd ..
root@:/usr/local/tomcat# cd webapps.dist
root@:/usr/local/tomcat/webapps.dist# ls
ROOT  docs  examples  host-manager  manager
root@:/usr/local/tomcat/webapps.dist# cp -R * ../webapps
root@:/usr/local/tomcat/webapps.dist# cd ..
root@:/usr/local/tomcat# ls
BUILDING.txt     LICENSE  README.md      RUNNING.txt  conf     lib   native-jni-lib  webapps       work
CONTRIBUTING.md  NOTICE   RELEASE-NOTES  bin          include  logs  temp            webapps.dist
root@:/usr/local/tomcat# cd webapps
root@:/usr/local/tomcat/webapps# ls
ROOT  docs  examples  host-manager  manager
root@:/usr/local/tomcat/webapps#
```
