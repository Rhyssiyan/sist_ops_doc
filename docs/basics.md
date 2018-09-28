## Unix常用命令
#### 系统信息
* 查看系统版本
    - lsb_release -a
    - uname -a 
* 系统运行状态
    * htop, top, glances皆可
    * 查看进程: ps -aux

#### 查看设备
* lshw
* 硬盘:
    - 查看硬盘挂载情况: ``df``,``lsblk``
    - 查看硬盘使用情况: ``du``
#### 网络情况
* 查看网卡信息:ifconfig
* 查看网络中存在的其他机器的ip和mac: arp -a
* 显示各种网络信息:
    - netstat -anp, 其中a为显示所有连接,p为查看进程
    - netstat -a 查看所有连接
    - netstat -ap pid 
    - netstat -l 查看哪些端口在监听
    - 查看路由表: netstat -r 或者 route
    - 查看dns服务器地址: cat /etc/resolv.conf
#### 显卡
* 动态查看显卡信息: watch -n 0.5 nvidia-smi 
* 查看cuda版本: cat /usr/local/cuda/version.txt
