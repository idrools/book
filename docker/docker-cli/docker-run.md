# docker run
Docker在隔离的容器中运行进程。 容器是在主机上运行的进程。 主机可以是本地主机，也可以是远程主机。 当操作员执行`docker run`时，运行的容器进程是独立的，因为它具有自己的文件系统，自己的网络以及独立于主机的独立的进程树。
## 通用格式
基本docker run命令的形式如下:
>$ docker run [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...]
docker run命令必须指定要从中派生容器的镜像，镜像开发人员可以定义与以下相关的图像默认值:
