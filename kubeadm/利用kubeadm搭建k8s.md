
#环境准备

192.168.1.215 master
192.168.0.176 worker1
192.168.0.175 worker2

修改hostname
   /etc/hostname
ssh配置 
   ssh-keygen -t rsa 添加id_rsa.pub到另外两台机器的authorized_keys中
修改hosts
   /etc/hosts

# 安装

**查询kubeadm文档** 
https://github.com/kubernetes/kubeadm/blob/master/docs/design/design_v1.10.md

**下载kubernetes 稳定版本**(倒数第二个版本) 
https://github.com/kubernetes/kubernetes/releases  

## 禁用防火墙
systemctl stop firewalld.service     # 停止firewall
systemctl disable firewalld.service  # 禁止firewall开机启动
systemctl stop iptables.service      # centos7不需要
systemctl disable iptables.service   # centos7不需要

## 配置yum安装仓库

**镜像站**
清华: https://mirrors.tuna.tsinghua.edu.cn/
阿里: https://mirrors.aliyun.com
-->
https://mirrors.aliyun.com/kubernetes/yum/repos/kubernetes-el7-x86_64/





