Docker basic command
                         ---DOCKER PULL---
1) docker pull = Pull an image or a repository from a registry

                    ---LIST CONTAINERS, IMAGES---
2) docker ps = Lists containers
3) docker ps -a = Lists running and stopped container
4) docker images = List images 
5) docker ps -aq = in ra tat ca containerID

                    ---START AND STOP CONTAINER---
6) docker start containerId = Start stopped containers
7) docker stop containerID = Stop one or more running containers

                         ---DOCKER RUN---
8) docker run image = Run a command in a new container || pulls image and starts container
9) docker run -d image = Run the command but can still continue writing other commands 
10) docker run -pPort:Port = Run a command on speciffic port
11) docker run image:version = Pull and run the container version you want

                        ---DOCKER DEBUGS---
12) docker logs containerId = Fetch the logs of a container
13) docker exec -it containerId /bin/bash (ls, pwd, cd/, ls, env, exit ) = Check details information inside image

                        ---DOCKER NAME---
14) docker run --name newName image = Run a command and change container name

                    ---REMOVE CONTAINER, IMAGE---
15) docker rm containerID/Name = xoa container duoc chi dinh
16) docker rm $(docker ps -aq) = xoa het tat ca container
17) docker rm -f $(docker ps -aq) = xoa het tat ca container ke ca khi dang chay
              
                    ---FORMAT---
18) docker ps --format=$FORMAT = format cho de nhin

                    ---VOLUMNS---
19) C:\website>docker run --name website -v "%CD%":/usr/share/nginx/html:ro -d -p 8080:80 nginx = ví dụ vể docker volumes sử dụng file index.html trong folder website thay vì file gốc của nginx
