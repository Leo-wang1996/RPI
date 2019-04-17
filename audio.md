# 				树莓派声卡驱动安装

查询播放设备命令：

aplay -l

驱动安装：

git clone https://github.com/respeaker/seeed-voicecard cd seeed-voicecard sudo ./install.sh  sudo reboot

安装完成，调整麦克风声音：

命令：alsamixer

测试：

arecord -Dac108 -f S32_LE -r 16000 -c 4 a.wav (4-mic)

cat /proc/asound/cards