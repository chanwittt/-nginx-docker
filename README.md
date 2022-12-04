## nginx-docker
### Source from https://github.com/armsultan
### Pre-required
#### 1. Download key and certificate files from F5 Portal
#### 2. Rename it to nginx-repo.key, nginx-repo.cert and keep it a same folder with Dockerfile
#### 3. Create nginx configuration file (default.conf) in same folder with Dockerfile
#### Work dir
##### - Dockerfile.nginx.centos8
##### - default.conf
##### - nginx-repo.key
##### - nginx-repo.crt
### Build
docker build --no-cache -t nginx-plus:centos8 -f Dockerfile.nginx.centos8 .

### Run
docker run -it -d -p 80:80 --name nginx-plus1 nginx-plus:centos8 /bin/bash

