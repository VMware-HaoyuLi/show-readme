# Network ports
* 80
* 443

# Software
* ubuntu 16.04
* git
* docker
* docker-compose

# Installation Steps
1. add ssh key
2. git clone git@github.com:vmware/flowgate.git
3. cd flowgate/make
4. bash build.sh all -version v1.0

# run
1. bash flowgate_run.sh
2. access https://hostname to visit

# down
* docker-compose -f maven-docker-build/docker-compose.run.images.yml down

# issue
## 1. curl#6: Couldn't resolve host name.
### add two nameserver to /etc/resolv.conf
1. nameserver 10.195.12.31
2. nameserver 10.172.40.1
