```bash
# 查看所有已经存在的镜像
docker images

# 创建一个新容器 直接拉取一个pytorch的已存在的镜像
docker run --gpus all -it -v /public/home/<yourPersonalPath>:/home/<yourPersonalPath> pytorch/pytorch

# 退出容器快捷键
ctrl + p + q

# 查看创建的镜像
docker ps
#-a :显示所有的容器，包括未运行的。
#-l :显示最近创建的容器。

# 将需要的文件拷贝进docker中的wzh文件夹
docker cp /public/home/<yourPersonalPath>/ <yourContainerID>:/<yourPersonalPath>/

# 进入容器内部 获得管理员权限
docker exec -it <yourContainerID> /bin/bash
```