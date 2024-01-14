## aliyun ECS

## CentOS环境下镜像编译

```text
yum update -y

sudo yum install -y yum-utils \
    device-mapper-persistent-data \
    lvm2

yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo

service docker start
docker ps

yum install git 
git clone https://github.com/SaifAati/Geospatial-COSICorr3D

```
# 下载docker compose

```
curl -L https://github.com/docker/compose/releases/download/v2.4.1/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose

```
# 添加可执行权限

```
sudo chmod +x /usr/local/bin/docker-compose
# 将文件copy到 /usr/bin/目录下
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
# 查看版本
docker-compose --version

docker-compose -f  docker-compose.yml build geocosicorr3d
```