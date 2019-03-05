# HomeAssistant
尝试家居智能化入门学习
尝试过“米家设备通过homebridge+homekit+Siri“控制，但是感觉不太好用：
1）不如iOS上米家APP+Siri捷径来得方便；
2）homekit对通过homebridge接入的设备状态更新有些不够快速还会有假死的状态（不知道是homebridge还是homekit的问题？），一言难尽。
决定抛弃homebridge，改用homeassistant...

运行环境：
1，PC（Ubuntu18）
2,米家智能设备若干...
3,iPad
4,iPhone

安装HomeAssistant
https://www.home-assistant.io/docs/installation/virtualenv/

以上安装全是坑

ubuntu18.04安装homeassistant
完美安装homeassistant需要python3.5

1.安装python3.5
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt-get update
sudo apt-get install python3.5
即使你本来电脑上安装了其他版本python也没关系，运行上面3条指令就好

2.安装python3.5-venv
sudo apt-get install python3.5-venv

3.创建并启用虚拟环境
我创建在/opt/hass下，你也可以换一个目录

cd /opt
sudo mkdir hass
cd /hass
sudo python3.5 -m venv .
source bin/activate
注意第4条指令最后有个点

4.安装一个python包
sudo python3.5 -m pip install wheel  
The directory &apos;/home/android/.cache/pip/http&apos; or its parent directory is not owned by the current user and the cache has been disabled. Please check the permissions and owner of that directory. If executing pip with sudo, you may want sudo&apos;s -H flag.
The directory &apos;/home/android/.cache/pip&apos; or its parent directory is not owned by the current user and caching wheels has been disabled. check the permissions and owner of that directory. If executing pip with sudo, you may want sudo&apos;s -H flag.
如果出现以上提示用sudo -H
sudo -H python3.5 -m pip install wheel
5.安装并启动homeassistant
sudo pip3 install homeassistant
hass --open-ui

配置文件在 Config directory: /home/android/.homeassistant
如果要退出虚拟环境，在Terminal输入deactivate
