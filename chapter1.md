---
description: 主要写一些环境配置的过程
---

# 搭建机器环境

## docker安装

下载docker for mac 18.03.1-ce-mac65:

```
官网下载：https://www.docker.com/docker-mac
```

## docker常用命令

```bash
# 下载对应的docker镜像
$: docker pull centos:6
# 列出当前的全部镜像
$: docker image ls
# 删除 image 文件
$: docker image rm [imageName]
# docker run 新建容器，每运行一次，就会新建一个容器
# -v 指定宿主机和docker容器共享文件 -it 指定终端打开docker
$: docker run -v /Users/bubble/workspace/docker/software:/software -it centos:6
# -p 指定宿主机和docker容器端口映射关系 --rm参数，在容器终止运行后自动删除容器文件
$: docker run --rm -p 8888:8888 dimajix/jupyter-spark:latest
# 列出当前的全部容器
$: docker container ls --all
# 移除指定容器
$: docker container rm [containerID]
# 停止指定的容器运行
$: docker container kill [containerID]
# 它用来启动已经生成、已经停止运行的容器文件。
$: docker container start [containerID]
# 命令也是用来终止容器运行，相当于向容器里面的主进程发出 SIGTERM 信号，然后过一段时间再发出 SIGKILL 信号。
$: docker container stop [containerID]
# 用于进入一个正在运行的 docker 容器
$: docker container exec -it [containerID] /bin/bash
# 用于从正在运行的 Docker 容器里面，将文件拷贝到本机
$: docker container cp [containID]:[/path/to/file]
# 保存用户对容器的修改
$: docker commit [containID] centos:6
```



{% hint style="info" %}
 Super-powers are granted randomly so please submit an issue if you're not happy with yours.
{% endhint %}

Once you're strong enough, save the world:

```
// Ain't no code for that yet, sorry
echo 'You got to trust me on this, I saved the world'
```



