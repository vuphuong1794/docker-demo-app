                         ---DOCKER PULL---
1) docker pull = Pull an image or a repository from a registry

                    ---LIST CONTAINERS, IMAGES---
2) docker ps = Lists containers
3) docker ps -a = Lists running and stopped container
4) docker images = List images 

                    ---START AND STOP CONTAINER---
5) docker start containerId = Start stopped containers
6) docker stop containerID = Stop one or more running containers

                         ---DOCKER RUN---
7) docker run image = Run a command in a new container || pulls image and starts container
8) docker run -d image = Run the command but can still continue writing other commands 
9) docker run -pPort:Port = Run a command on speciffic port
10) docker run image:version = Pull and run the container version you want

                        ---DOCKER DEBUGS---
11) docker logs containerId = Fetch the logs of a container
12) docker exec -it containerId /bin/bash (ls, pwd, cd/, ls, env, exit ) = Check details information inside image

                        ---DOCKER NAME---
12) docker run --name newName image = Run a command and change container name