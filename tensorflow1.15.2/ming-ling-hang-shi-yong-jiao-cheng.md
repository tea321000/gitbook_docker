# 命令行使用教程



1. 在终端中输入tensorflow\_docker\_bash，运行tensorflow1.15.2的docker：

![](../.gitbook/assets/image%20%286%29.png)

2.如同宿主机的终端使用即可，同notebook，容器的/tf实际映射到宿主机的/host/tf，使用`python xx.py`进行py文件的执行。

3.要注意的是在不使用container时记得使用`sudo docker ps`查看正在运行的容器，并使用`sudo docker stop`和`sudo docker rm`停止和删除容器。

