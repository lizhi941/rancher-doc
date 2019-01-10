# Install_rancher.md


##  System parameter

* OS system: Ubuntu Description: Ubuntu 16.04.5 LTS Release: 16.04 Codename: xenial
* Docker version:docker-ce-17.03.2.ce

## Install

```
docker run -d --restart=unless-stopped -p 8080:80 -p 8443:443 rancher/rancher:v2.1.5

```
