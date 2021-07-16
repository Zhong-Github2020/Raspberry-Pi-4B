# 解决个别wifi连不上问题
个别wifi连不上，而且wifi的信号时隐时现，但别的路由器可以连的上。
基于这种现象，排除硬件问题。<br>
是否因为原来的路由器，信道问题？<br>
```
pi@raspberrypi:~ $ iwlist wlan0 freq 
wlan0     18 channels in total; available frequencies : 
          Channel 01 : 2.412 GHz 
          Channel 02 : 2.417 GHz 
          Channel 03 : 2.422 GHz 
          Channel 04 : 2.427 GHz 
          Channel 05 : 2.432 GHz 
          Channel 06 : 2.437 GHz 
          Channel 07 : 2.442 GHz 
          Channel 08 : 2.447 GHz 
          Channel 09 : 2.452 GHz 
          Channel 10 : 2.457 GHz 
          Channel 11 : 2.462 GHz 
          Channel 12 : 2.467 GHz 
          Channel 13 : 2.472 GHz 
          Channel 149 : 5.745 GHz 
          Channel 153 : 5.765 GHz 
          Channel 157 : 5.785 GHz 
          Channel 161 : 5.805 GHz 
          Channel 165 : 5.825 GHz 
          Current Frequency:2.472 GHz (Channel 13) 
```
进入路由器设定界面，目前使用的K3C路由器是可以有两个SSID的，因此选取其中一个将信道从“自动”改为上面Channel中的一个。（本例改为161）<br>
在树莓派的wifi设定中，选取信道为161的SSID，输入密码。<br>
成功！<br>
