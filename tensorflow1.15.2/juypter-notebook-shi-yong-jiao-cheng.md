# jupyter notebook使用教程

1. 在终端中输入tensorflow\_docker，运行tensorflow1.15.2的docker：

![](../.gitbook/assets/image%20%281%29.png)

2.复制终端显示的下方最后的链接`http://127.0.0.1:8888/?token=8c0564cee06649c6fff6cede8976579813330a7a7fdea8df`将其本机IP 127.0.0.1改为服务器静态IP 192.168.123.137，即改为`http://192.168.123.137:8888/?token=8c0564cee06649c6fff6cede8976579813330a7a7fdea8df`

![](../.gitbook/assets/image%20%282%29.png)

3.在浏览器中粘贴该链接，进入jupyter notebook界面。

![](../.gitbook/assets/image%20%283%29.png)

其实际映射到host的路径为/host/tf ，可以将notebook文件夹软链接\(推荐\)或者复制到该文件夹中进行执行。

4.在notebook中也可以执行linux命令，在需要执行的linux命令前面加感叹号!即可执行

```python
# 在需要执行的linux命令前面加感叹号!即可执行
!nvidia-smi

import tensorflow as tf
#输出版本号
print(tf.__version__)

from tensorflow.python.client import device_lib
def get_available_gpus():
    local_device_protos = device_lib.list_local_devices()
    return [x.name for x in local_device_protos if x.device_type == 'GPU']

# 显示当前可用GPU
get_available_gpus()
```

5.结束使用时记得在终端中按Ctrl+C 停止notebook server的运行

