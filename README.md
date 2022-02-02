# Raspberry-Pi-4B
Run Linux in Raspberry Pi 4B (8G)<br>
###### 安装中文输入法<br>
在终端窗口，输入：<br>
`
sudo apt-get install -y fcitx-googlepinyin
`
<br>
###### 安装firefox ESR<br>
在终端窗口，输入：<br>
`
sudo apt-get install firefox-esr -y
`
<br>
对32位版本的Pi OS来说，SMB协议已经更新到2.0版本以上。移动硬盘挂载在路由器上时，会使用SMB1.0.所以采用挂载的方式：<br>
`
sudo mount -t cifs -o guest,vers=1.0 //K3C/Disc-1/ /home/pi/K3C/
`<br>
[参考链接](https://blog.csdn.net/zjy0856/article/details/86745635)
