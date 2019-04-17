# 			树莓派摄像头驱动安装

sudo raspi-config

打开Camera

sudo nano /etc/modules

bcm2835-v4l2

vcgencmd get_camera

raspistill -t 2000 -o 1.jpg