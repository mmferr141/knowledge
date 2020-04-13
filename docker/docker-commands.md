# Docker commands

## Docker commands

### Run a container

sudo docker run \[image\] \[command\] sudo docker run redis redis-server

### Run a container and show output

sudo docker run -a \[image\] \[command\] sudo docker run -a redis redis-server

### Run a container with input open

sudo docker run -it \[image\] \[command\] sudo docker run -it redis sh

### Create a container

sudo docker create \[image\] \[command\] sudo docker create redis redis-server

### Starts a container

sudo docker start \[container id\] sudo docker start 45abc9o10b11uio0

### Starts a container and show output

sudo docker start -a \[container id\] sudo docker start 45abc9o10b11uio0

### Executes a command in a running container

sudo docker exec \[container id\] \[command\] sudo docker exec 45abc9o10b11uio0 ping google.com

### Executes a command in a running container with input open

sudo docker exec -it \[container id\] \[command\] sudo docker exec -it 45abc9o10b11uio0 redis-cli

### Builds a container

sudo docker build \[docker build directory\] sudo docker build .

### Builds a container with tag name

sudo docker build -t \[user/image-name:version\] \[docker build directory\] sudo docker build -t mferreira/redis:latest .

### List processes in execution

sudo docker ps

### List history of processes

sudo docker ps --all

### See logs of a specific container

sudo docker logs \[container-id\] sudo docker logs 45abc9o10b11uio0

### Commit  a command to a container in order to create a new one

sudo docker commit -c 'CMD \["package-name"\]' sudo docker commit -c 'CMD \["redis-server"\]'

