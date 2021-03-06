
## 数据存储结构总览
![](img/data.png)

## 网络拓扑结构总览
所有计算节点的GPU使用情况可以在[GPU Status](http://10.19.124.11:8899/gpu)中查看

| AI集群内网IP | 节点名字 | CPU | MEM |         GPU         |         说明         |
| :----------: | :------: | :-----------------:  | :-----------------:  | :-----------------:  | :-----------------:  |
| 10.10.10.100 |  admin   | 56 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz |  251G  |      None      |       管理节点    |
| 10.10.10.200 |    io    |    40 cores  Intel(R) Xeon(R) CPU E5-2650 v3 @ 2.30GHz    |    62G    |       None       |       存储节点    |
| 10.10.10.101 |  node01  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  251G  |   M40 x 4    |  计算节点 |
| 10.10.10.102 |  node02  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  251G  |   M40 x 4    |  计算节点 |
| 10.10.10.103 |  node03  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  251G  |   M40 x 4    |  计算节点 |
| 10.10.10.104 |  node04  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  251G  |   M40 x 4    |  计算节点 |
| 10.10.10.105 |  node05  |  28 cores Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz   |  188G  | GTX1080 x 4  | 计算节点 |
| 10.10.10.106 |  node06  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  188G  | GTX1080 x 4  | 计算节点 |
| 10.10.10.107 |  node07  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  188G  | GTX1080 x 4  | 计算节点 |
| 10.10.10.108 |  node08  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  | 188G | GTX1080 x 4  | 计算节点 |
| 10.10.10.109 |  node09  |  56  cores Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  188G  | TITAN XP x 4 | 计算节点 |
| 10.10.10.110 |  node10  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  188G  | TITAN XP x 4 | 计算节点 |
| 10.10.10.111 |  node11  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  188G  | GTX1080 x 4  | 计算节点 |
| 10.10.10.112 |  node12  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  188G  | GTX1080 x 4  | 计算节点 |
| 10.10.10.113 |  node13  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  251G  |   K80 x 8    |  计算节点 |
| 10.10.10.114 |  node14  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  251G  |   K80 x 8    |  计算节点 |
| 10.10.10.115 |  node15  |  56  cores Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  251G  | GTX1080 x 4  | 计算节点 |
| 10.10.10.116 |  node16  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  251G  | GTX1080 x 4  | 计算节点 |
| 10.10.10.117 |  node17  |  28 cores  Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  251G  | GTX1080 x 4  | 计算节点 |
| 10.10.10.118 |  node18  |  56  cores Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz  |  251G  | GTX1080 x 4  | 计算节点 |

## Docker Container 内置环境
| 环境     | 版本        | 环境      | 版本      |
| :----------------: | :-----------: | :---------------: | :----------: |
| [ubuntu](https://www.ubuntu.com/)                 | 16.04.4 LTS | [nvidia driver](https://www.nvidia.com/object/unix.html) | 387.26 ( 不可更改) |
| [cuda](https://developer.nvidia.com/cuda-zone)    | 9.0.176     | [cudnn](https://developer.nvidia.com/cudnn)                 | 7.1.4              |
| [python](https://www.python.org/)                 | 3.6.6       | [tensorflow](http://www.tensorflow.org/)                    | 1.9.0              |
| [pytorch](http://pytorch.org/)                    | 0.4.0       | [mxnet](http://mxnet.incubator.apache.org/)                 | 1.2.1              |
| [keras](https://keras.io/)                        | 2.2.2       | [lasagne](http://lasagne.readthedocs.io/)                   | 0.2.dev1           |
| [cntk](http://cntk.ai/)                           | 2.5.1       | [chainer](https://chainer.org/)                             | 4.3.1              |
| [caffe](http://caffe.berkeleyvision.org/)         | 1.0.0       | [caffe2](https://caffe2.ai/)                                | 0.8.2              |
| [torch](http://torch.ch/)                         | 7           | [sonnet](https://github.com/deepmind/sonnet)                | 1.23               |
| [theano](http://deeplearning.net/software/theano) | 1.0.1       |                                                             |                    |




## 组件

### 显卡

#### 显卡性能概览
深度学习对高性能GPU有非常大的需求, 而AI集群中又有各种版本的GPU, 故在此给出简单测试结果, 供大家参考.

**测试环境**: CUDA9.0 + Pytorch0.4 + VGG16 跑Cifar10  
**分数标准**: 以K80性能为一个基本单位, 可以简单地理解为运算速度, 如P40分数为11.57, 说明同样的网络K80跑一个epoch, P40可以跑11.57个epoch.

![](img/gpu_test.png)

### cpu及内存

* cpu: Intel(R) Xeon(R) CPU E5-2690 v4 @ 2.60GHz(14核)
* 大部分节点256G,部分节点比如node 10少些，只有189G

### 网络
* 网卡:ib网卡
* 网络实测带宽：8.36 Gbits/sec
  
    ``iperf -u -c 12.12.12.200 -b 100000M -t 60 -i 10`` 


### 磁盘
* ``df``指令可查询文件系统的挂载情况
* 大小: 80T
#### 磁盘io
* 磁盘阵列为RAID 5
* io测速:
    
    ![](img/admin_disk_io.png) 
  
## 架构介绍
为安全考虑, AI集群上分admin和计算节点两种.所有节点的容器都是通过ib网卡访问80T存储.每个用户有一部分计算节点权限,其不同节点间的同步是由不同节点上的该用户的容器的对应目录都映射到同一个目录中保证的。举个例子,
不同节点容器的/bin文件夹都映射到属于该用户的同一个bin文件.

* [Source Code](https://github.com/piaozhx/DockerMonitor)
    - 前端: tornado
    - 数据库: mysql
    - 容器化管理: docker
    - GPU,CPU等监控系统: gpu_tools文件夹下

### 监控系统


### 容器
* [容器配置](https://github.com/piaozhx/DockerMonitor/blob/master/handler/permission_handler.py)
     