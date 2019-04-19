
# Network ports

|Port|Protocol|Description|
|---|---|---|
|443|HTTPS|Flowgate will accept requests on this port for https protocol|
|80|HTTP|Flowgate will accept requests on this port for http protocol|

# Software

|Software|Version|Description|
|---|---|---|
|Ubuntu|version 16.04|ubuntu 16.04|
|Git|version 2.7.4 or higher|For installation instructions, please refer to: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git|
|Docker|version 18.09.2 or higher|For installation instructions, please refer to: https://docs.docker.com/engine/installation/|
|Docker-compose|latest is preferred|For installation instructions, please refer to: https://docs.docker.com/compose/install/|

# Installation Steps
1. generating a SSH keys for your git clone
```
2. git clone git@github.com:vmware/flowgate.git
```
```
3. cd flowgate/make
```
```
4. bash build.sh all -version v1.0
```

# run
```
1. bash flowgate_run.sh
```
2. access https://hostname to visit

# down
``` 
docker-compose -f maven-docker-build/docker-compose.run.images.yml down
```

# issue
## 1. curl#6: Couldn't resolve host name.
### add two nameserver to /etc/resolv.conf
1. nameserver 10.195.12.31
2. nameserver 10.172.40.1
