<h1 align="center">Docker basic command</h1>

<h2 align="center">DOCKER PULL</h2> 
1) docker pull = Pull an image or a repository from a registry

<h2 align="center">LIST CONTAINERS, IMAGES</h2>
2) docker ps = Lists containers
3) docker ps -a = Lists running and stopped container
4) docker images = List images 
5) docker ps -aq = in ra tat ca containerID

<h2 align="center">START AND STOP CONTAINER</h2>
6) docker start containerId = Start stopped containers
7) docker stop containerId = Stop one or more running containers

<h2 align="center">DOCKER RUN</h2>
- docker run [OPTIONS] ${IMAGE_NAME}:${IMAGE_TAG} command
- ex: docker run -it ubuntu:18.04 sh 
8) docker run image = Run a command in a new container || pulls image and starts container
9) docker run -d image = Run the command but can still continue writing other commands 
10) docker run -p Port:Port = Run a command on speciffic port
11) docker run image:version = Pull and run the container version you want

<h2 align="center">DOCKER DEBUGS</h2>
12) docker logs containerId = Fetch the logs of a container
13) docker exec -it containerId /bin/bash (ls, pwd, cd/, ls, env, exit ) = Check details information inside image

<h2 align="center">DOCKER NAME</h2>
14) docker run --name newName image = Run a command and change container name

<h2 align="center"> REMOVE CONTAINER, IMAGE</h2>
15) docker rm containerId/Name = xoa container duoc chi dinh
16) docker rm $(docker ps -aq) = xoa het tat ca container
17) docker rm -f $(docker ps -aq) = xoa het tat ca container ke ca khi dang chay
              
<h2 align="center">FORMAT</h2>
18) docker ps --format=$FORMAT = format cho de nhin

<h2 align="center">VOLUMNS (duy trì dữ liệu bên trong container</h2>
19) C:\website>docker run --name website -v "%CD%":/usr/share/nginx/html:ro -d -p 8080:80 nginx = ví dụ vể docker volumes sử dụng file index.html trong folder website thay vì file gốc của nginx
20) ví dụ lưu dữ liệu cho mongo
    + mkdir data (tạo folder lưu dữ liệu)
    + docker run -it -p 27017:27017 -v $(pwd)/data:/data/db --name mongo -d mongo
ví dụ khi container bị lỗi hay ngưng hoạt động hay db bị dừng thì dữ liệu vẫn được duy trì mà ko bị mất
