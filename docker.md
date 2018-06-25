
```
yum install -y yum-utils device-mapper-persistent-data lvm2
```
```
yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```
```
yum-config-manager --enable docker-ce-edge
```
```
yum-config-manager --disable docker-ce-test
```
```
yum install docker-ce
```
```
systemctl start docker
```
```
docker run hello-world
```
```
systemctl enable docker
```
