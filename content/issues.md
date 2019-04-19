# Issues

## 当rancher server所占的磁盘空间过大时如何处理 ？
1：首先查看大小
```
下面命令会显示容器大小
sudo docker ps -s

```
2：删除其log所占的空间，假设其所在的容器id是oi098hioih,docker容器的存储路径是/var/lib/docker/containers;

```
truncate -s 0 /var/lib/docker/containers/oi098hioih/*-json.log

```

##
##
##
