---
title: CentOS 笔记
tags: Linux
categories: Note
top: 80
abbrlink: 875db5e1
date: 2019-05-25 18:09:05
---

![CentOS-笔记](http://qiniuyun.lintstar.top/CentOS-笔记.png)
#### CentOS 常用命令
- `shutdown -h now`             关机
- `shutdown -h +3`              三分钟后关机
- `halt`
- `poweroff`
- `init 0`

- `shutdown -r now`             重启
- `shutdown -r +3`              三分钟重启
- `reboot`
- `init 6`

- `cat 1.txt | tail - n +3001 | head -n 1000`                       截取文件中的3001到4000

- `grep o 1.txt`                正常过滤
- `grep -v 1.txt`               反向过滤

- `cat >1.txt`                  清空文件内容
- `ll -d /data/www`             查看权限

- `pkill -kill -t tty3`          杀死用户进程

- `mkdir /media/cdrom`
- `mount /dev/sr0  /media/cdrom`             挂载光盘
- `umount /media/cdrom`                      卸载

- `systemctl stop firewalld.service`         关闭防火墙
- `setenforce 0`                             给外界权限
- `systemctl disable firewalld.service`      永久关闭
- `systemctl enable firewalld.service`       永久开启
- `vim /etc/rc.d/rc.local`                   设置开机启动
为镜像添加开机自动挂载
- `echo "mount /dev/sr0  /media/cdrom" >> /etc/rc.d/rc.local`


- `vim /etc/selinux/config`
- `^vim^cat`                        把vim替换成cat继续执行

- `ls -al`                          看临时文件

#### CentOS7 目录文件
* `/etc/yum.repos.d/`                   yum源文件位置
* `/etc/rc.d/rc.local`                  开机启动文件
* `rm -f /var/run/yum.pid`
* `yum clean all`                       清空yum源缓存
* `/etc/nginx/conf.d/default.conf`      Nginx配置文件
* `vim /etc/my.cnf`                     去mysql密码要求
* `/usr/share/nginx/html/`              Nginx主页文件位置
* `/etc/httpd/conf/httpd.conf`          Apache配置文件
* `/var/www/html/`                      Apache主页文件位置