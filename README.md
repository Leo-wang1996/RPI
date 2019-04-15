# 			树莓派使用笔记

树莓派使用笔记

树莓派基金会：<https://www.raspberrypi.org/>

1、下载系统

<http://shumeipai.nxez.com/download#os>

2、写入系统（Win32DiskImager）

使用工具win32DiskImager写入完成后

使用Windows powershell开启ssh

命令：new-item ssh -type file （创建在uefi分区）

(win7 使用 git bash    touch ssh）

3、更换源

sudo nano /etc/apt/sources.list

<https://mirrors.tuna.tsinghua.edu.cn/help/raspbian/>

选择对应于系统的版本

4、安装git

sudo apt install git

5、python脚本获取树莓派状态

<http://shumeipai.nxez.com/2014/10/04/get-raspberry-the-current-status-and-data.html>

6、运行raspi-config

修改root密码，扩大分区等

7、树莓派开启wifi热点

git clone <https://github.com/oblique/create_ap>

cd create_ap

sudo make install

安装依赖库：

apt-get install util-linux procps hostapd iproute2 iw haveged dnsmasq

开启热点：create_ap wlan0 eth0 MyAccessPoint

（详细使用见github）

8、远程桌面

sudo apt install xrdp

9、修改swap空间

sudo nano /etc/dphys-swapfile  < change CONF_SWAPSIZE=100 to CONF_SWAPSIZE=1024 and save / exit nano >  sudo /etc/init.d/dphys-swapfile restart

