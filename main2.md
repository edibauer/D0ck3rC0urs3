### 04
```bash
docker run nginx
docker ps
docker ps -a

```
#### Second plane
```bash
docker run -d nginx
# ans: hash
docker ps
docker logs <hash>
docker logs -f <hash> # live
docker attach <hash> # live without entering container

docker run -d --restart=always nginx # restart when mahcine restarts

```
#### port forwarding
```bash
docker run -d -p 8080:80 nginx # local:container


```
#### Bonus
```bash
docker run -d -p 8080:80 nginx # local:container

```
### 05
```bash
docker exec <hash> ls
docker exec <hash> whoami
docker exec <hash> id

docker exec -it 605ef914b5b9 bash

docker stop 605ef914b5b9

docker run -d --name web1 -p 8080:80 nginx  #naming containers. we can repeat names and ports

docker rm web2
docker container prune # remove stopped containers

```

### 06
```bash
docker pull nginx
docker image prune # deletes images without asociated containers
docker image prune -a

docker search nginx
```

### 07
![alt text](image.png)
```bash
docker build . -t app-nginx # build images
docker run -d --name web -p 8080:80 app-nginx # create container

localhost:8081/index.html

docker build -t app-python .
docker run -it app-python

# execution order
# most changed to minus changed like (like scripts)


```