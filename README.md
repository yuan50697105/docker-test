# 通用注意事项

- 安装Docker
- Cent OS 7

```shell
  更新依赖
  sudo yum update
  删除旧版docker
  sudo yum remove docker  docker-common docker-selinux docker-engine
  sudo yum install -y yum-utils device-mapper-persistent-data lvm2
  sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
  sudo yum install docker-ce
  
  sudo systemctl start docker
  sudo systemctl enable docker
  安装docker-compose
  sudo yum install docker-compose
```

- Cent OS 8

```shell
sudo yum install -y yum-utils  device-mapper-persistent-data  lvm2
 
sudo yum-config-manager  --add-repo   https://download.docker.com/linux/centos/docker-ce.repo
 
sudo yum install docker-ce docker-ce-cli containerd.io
```

- Ubuntu

```shell
卸载可能存在的旧版本
sudo apt-get remove docker docker-engine docker-ce docker.io

更新apt包
sudo apt-get update

通过HTTPS使用仓库(repository)安装
sudo apt install apt-transport-https ca-certificates curl software-properties-common

在/etc/apt/sources.list.d/docker.list文件中添加下面内容
deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable

添加Docker官方的GPG密钥
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

安装
sudo apt install docker-ce
```

- ## 开启远程

```
访问并修改Docker配置文件  
vi /lib/systemd/system/docker.service　

```
<img src="C:\Users\Administrator\Downloads\1817484-20190926214747673-507823979.png" alt="1817484-20190926214747673-507823979" style="zoom: 67%;" />

```shell
修改daemon.json  
vi /etc/docker/daemon.json
```

<img src="C:\Users\Administrator\Downloads\1817484-20190926224044817-2131152622.png" alt="1817484-20190926224044817-2131152622" style="zoom: 80%;" />

```shell
刷新配置并重启服务

　　　　systemctl daemon‐reload

　　　　systemctl restart docker
```




- ## 修改虚拟内存

```shell
sysctl -w vm.max_map_count=262144
```



- ## 授权

```shell
chmod 777 xxxx路径
```

- ## Docker Shell

- ## Dockerfile

- ## Docker-Compose

```shell
docker-compose up -d
```

- ## Docker Swarm



# elasticsearch

## 7.6.1

## 6.8.1

# solr

## 8.4

# influxdb

## 1.7

# mongo

## 3-xenial

## 4-bionic

# mysql

## 8.0

## 5.7

## mariadb

### 10.5.1

# nginx

# postgres

## 12

## 11

## 10

## 9

# rabbitmq

## 3.8

# redis

## 5.0.8

# tomcat

## 8-jdk8

## 8-jdk11

## 9-jdk8

## 9-jdk11

# jetty

## 9-jre8

## 9-jre11
