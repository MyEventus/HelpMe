---  
last_update: 2023Apr16  
share: true    
---  
  
Related:   
![Docker_Concept](./Docker_Concept.md)  
  
  
# Docker general cheatsheet Note:   
These are global commands and you can run them from anywhere.  
  
## Restart Docker Service  
sudo service docker restart  
  
## Containers-Show Running  
docker ps  
  
## Containers-Show All  
docker ps -a  
  
## Real Time Stats.  
docker stats  
  
## Containers-Delete / Remove  
docker ps -a  
docker stop <container_name>  
docker rm   
  
## Images-Delete / Remove  
docker images -a  
docker rmi <image_name>  
  
## Docker_Permissions_Group  
  
> sudo groupadd docker  
> sudo usermod -aG docker $USER  
  
# Recreate Container  
docker-compose up --build --force-recreate  
  
  
## Prune  
The docker system prune command removes all stopped containers, dangling images, and unused networks:  
  
  
docker system prune  
docker system prune -a (Not just dangling ones)  
Use the -f (--force) option to bypass the prompt.  
  
  
## Containers-Clear:   
docker rm -f $(docker ps -a -q)   
  
  
## Images-Clear:   
docker rmi -f $(docker images -a -q)   
  
  
## Good Reference Cheatsheet.  
https://oracle-base.com/articles/linux/docker-clean-up-unwanted-containers-images-layers-volumes-networks  
  
  
## Volumes-Clear:   
docker volume rm $(docker volume ls -q)   
  
  
## Networks-Clear:   
docker network rm $(docker network ls | tail -n+2 | awk '{if($2 !~ /bridge|none|host/){ print $1 }}')  
  
  
docker exec -it mycroft /bin/bash  
  
docker logs –follow mycroft  
  
  
## Start at boot.  
After docker 1.11, this is easy to fix  
  
docker update –restart=always my-container  
docker update –restart=no my-container  
  
  
  
## DOCKER GENERAL TIPS / HELP.  
  
  
## Create Dockerfile (Name Dockerfile)  
Add..  
  
FROM  
  
BUILD IMAGE  
docker build -t <create_tag_name> .  
  
RUN  
docker run -d -p 3001:27017 horka/mongodb  
docker run -it -e MONGO_URL=127.0.0.1:3001 -p 3000:3000 doc-met-te64-v1.00  
  
  
https://github.com/aedm/minimeteor  
  
  
docker run -d -e ROOT_URL=... -e MONGO_URL=... -p 80:3000 myDockerTag  
  
  
  
docker exec -it /bin/bash Unity Switcher Fix. (Alt - Tab)   
  
https://ubuntuforums.org/showthread.php?t=2211863   
  
  
## TO CREATE IMAGE  
  
Make "Dockerfile"  
FROM   
CMD ["echo", "hello world"]  
  
  
   
## TO CREATE SCRIPT OUTSIDE CONTAINER TO RUN  
  
 nano myscript.sh  
  
!/bin/sh  
echo Hello world outside container.  
  
  
## MAKE EXECUTABLE. sudo chmod +x myscript.sh   
  
  
docker build . docker run -name mynewcontainername <new_image_id>  
  
  
   
## Remove all non-running containers (delete).   
  
docker rm $(docker ps -a -f status=exited -q).    
  
  
## CREATE IMAGE FROM CONTAINER..   
  
sudo docker commit 2be21a3b5821 name-here/wd-nodered-template:v1.00   
  
  
## SAVE THE IMAGE TO A TAR FILE..   
  
sudo docker save -o cWorkID Al.H/wd-nodered-template:v1.00.tar name-here/wd-nodered-template:v1.00 or sudo docker save name-here/wd-nodered-template:v1.00 > wd-nodered-template.tar   
  
  
## MOVE FILE ON USB STICK TO TARGET.  
  
  
sudo docker load docker load < wd-nodered-template.tar   
  
  
## THEN TREAT AS YOU WOULD ANY IMAGE ON TARGE DEVICE.   
  
sudo docker run -it -p 1880:1880 name-here/wd-nodered-template:v1.00  
  
  
## Purging All Unused or Dangling Images, Containers, Volumes, and Networks  
Docker provides a single command that will clean up any resources — images, containers, volumes, and networks — that are dangling (not associated with a container):  
  
docker system prune  
  
  
To additionally remove any stopped containers and all unused images (not just dangling images), add the -a flag to the command:  
  
```  
docker system prune   
OR  
docker system prune -a  
```  
  
To confirm:  
```  
docker ps -a  
docker images -a  
---  
  
  
  
## DJANGO INSIDE DOCKER.  
  
sudo docker-compose run web django-admin startproject mysite .  
  
  
## UPDATE CONTAINER  
https://www.youtube.com/watch?v=76Xctfb_qI8  
OR  
Watcher  
