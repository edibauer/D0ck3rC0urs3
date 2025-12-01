### docker
#### start | stop
```bash
systemctl status docker
systemctl stop docker # sudo
systemctl start docker # sudo

```

#### docker command
```bash
docker version


```

#### Containers
- Virtual box that contain an app
```bash
docker run hello-world:latest

```

#### docker images
```bash

docker pull ubuntu:latest
docker run ubuntu # named: bold_wiles
docker start bold_wiles
docker exec -it bold_wiles bash

docker ps -a -q # show only id's

docker pull fedora:latest
docker run --name my_fedora fedora # own container name


```
#### Interactive containers
```bash
docker run -it --name sec_fedora fedora
docker 
# ans
[root@20cdb9f3fc22 /]# 

```

#### fazt
```bash
docker pull mysql
docker run --name own_mysql -e MYSQL_ROOT_PASSWORD=edibauer369 -d mysql

docker exec -it own_mysql bash



```