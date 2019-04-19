# Installation and Configuration Guide
Flowgate can be installed by one of three approaches: 
- **Online installer:** The installer downloads Harbor's images from Docker hub. For this reason, the installer is very small in size.

- **Offline installer:** Use this installer when the host does not have an Internet connection. The installer contains pre-built images so its size is larger.

All installers can be downloaded from the **[official release](https://github.com/goharbor/harbor/releases)** page. 

This guide describes the steps to install and configure Flowgate by using the online or offline installer.

 The installation processes are almost the same. 

## Prerequisites for the target host
Flowgate is deployed as several Docker containers, and, therefore, can be deployed on any Linux distribution that supports Docker. The target host requires  Docker, and Docker Compose to be installed. 

### Hardware
|Resource|Capacity|Description|
|---|---|---|
|CPU|minimal 2 CPU|4 CPU is preferred|
|Mem|minimal 4GB|8GB is preferred|
|Disk|minimal 40GB|160GB is preferred|

### Network ports

|Port|Protocol|Description|
|---|---|---|
|443|HTTPS|Flowgate will accept requests on this port for https protocol|
|80|HTTP|Flowgate will accept requests on this port for http protocol|

### Software

|Software|Version|Description|
|---|---|---|
|Ubuntu|version 16.04|ubuntu 16.04|
|Git|version 2.7.4 or higher|For installation instructions, please refer to: https://git-scm.com/book/en/v2/Getting-Started-Installing-Git|
|Docker|version 18.09.2 or higher|For installation instructions, please refer to: https://docs.docker.com/engine/installation/|
|Docker-compose|latest is preferred|For installation instructions, please refer to: https://docs.docker.com/compose/install/|

## Installation Steps

The installation steps boil down to the following

1. download the source code
2. run build script under make folder 


1. git clone git@github.com:vmware/flowgate.git
2. cd flowgate/make
3. bash build.sh all -version v1.0


# run
```
1. bash flowgate_run.sh
```
2. access https://hostname to visit

# down
``` 
docker-compose -f maven-docker-build/docker-compose.run.images.yml down
```
# Login
* default username admin , password Admin!23
* access https://hostname to visit
# issue
## 1. curl#6: Couldn't resolve host name.
### add two nameserver to /etc/resolv.conf
1. nameserver 10.195.12.31
2. nameserver 10.172.40.1
