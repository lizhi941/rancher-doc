# Delete

## How to delete a rancher client

* 1.Delete it on the rancher server

* 2.Login the host which the rancher client is on,delete the docker container

2.1 删除名字含有rancher的容器


```
#列出含有rancher名字的容器，并取出它们的id


sudo docker ps -a|grep rancher|awk '{print $1}'


#停止这些容器

sudo docker stop `docker ps -a|grep rancher|awk '{print $1}'`

#删除这些容器


sudo docker rm `docker ps -a|grep rancher|awk '{print $1}'`


```

* delete all volume belongs to the rancher client

* At last, delete the directory /var/lib/rancher

