# 基本操作

* 退出容器环境（没有杀死进程）：依次按下Ctrl+P，Ctrl+Q，此时python程序仍会继续执行
* 销毁容器环境（杀死进程）：输入exit，回车
* 查看运行中的容器及其ID：

  ```text
  sudo docker ps
  ```

* 假如在退出容器环境后还想还原原来的现场，则重新启动容器并attach附加至进程：

  ```text
  sudo docker start 容器ID
  sudo docker attach 容器ID
  ```

* 容器container是镜像image的实例化，停止运行即关闭容器进程。
* 停止容器：

  ```text
  sudo docker stop 容器ID
  ```

* 停止后可以用rm删除：

  ```text
  sudo docker rm 容器ID
  ```

由于docker的虚拟性，可以安装任意版本的tf\pytorch\mxnet而不冲突。需要安装旧版本的框架可以联系我。

