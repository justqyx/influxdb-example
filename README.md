InfluxDB && Grafana
---

## 安装 Docker 环境

```
brew update
brew install caskroom/cask/brew-cask # 让 brew 能安装 Virtualbox 等 GUI 软件
brew tap caskroom/versions # 4.3 版本的 virtualbox 配合 docker 更稳定一些，而不是 5.0 最新版
brew cask install virtualbox43691406

brew install docker-compose
brew install docker-machine # 使用 docker-machine 来管理 docker 容器
docker-machine create --driver virtualbox --virtualbox-boot2docker-url https://get.daocloud.io/boot2docker/boot2docker-lastest.iso default # 创建虚拟机 default

eval "$(docker-machine env default)"
```

## 拉取镜像

```
docker pull influxdb:alpine
docker pull grafana/grafana:3.0.3
```


## 启动服务

```
docker-compose up
```
