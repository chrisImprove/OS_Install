# Ubuntu 16.04 环境搭建

### 一、卸载不必要的软件
1.删除libreoffice
```
sudo apt-get remove libreoffice-common
```
2.删除Amazon的链接
```
sudo apt-get remove unity-webapps-common
```
3.删掉基本不用的自带软件（用的时候再装也来得及）
```
sudo apt-get remove totem empathy brasero  gnome-mahjongg aisleriot gnome-mines cheese  gnome-orca webbrowser-app gnome-sudoku
"sudo apt-get remove thunderbird totem rhythmbox empathy brasero simple-scan gnome-mahjongg aisleriot gnome-mines cheese transmission-common gnome-orca webbrowser-app gnome-sudoku  landscape-client-ui-install
"sudo apt-get remove onboard deja-dup
```
> <small>thunderbird:邮件客户端&nbsp;&nbsp;&nbsp;&nbsp;totem:视频播放器  
rhythmbox:音乐播放器  
simple-scan:扫描易  
gnome-mahjongg:对对碰  
aisleriot:接龙游戏  
gnome-mines:扫雷  
cheese:茄子-使用摄像头来拍照和录像  
gnome-orca:屏幕阅读器  
webbrowser-app:浏览器  
gnome-sudoku:数读  
Empathy:是GNOME 桌面环境的官方即时消息程序。  
brasero:Brasero 是一款 GNOME 桌面下的 CD/DVD 刻录应用程序.  
onboard:屏幕按键  
deja-dup:备份</small>
### 二、安装常用的软件及程序  
1. 更新软件源及升级软件
```
sudo apt update
sudo apt upgrade
```
2. 安装常用软件程序
```
sudo apt install nginx
sudo apt install php7.0 (except php7.0-snmp)
sudo apt install mysql-server

sudo apt install git
sudo apt install vim
sudo apt install curl
curl https://raw.githubusercontent.com/chrisImprove/vim/master/bootstrap.sh > bootstrap.sh && sh bootstrap.sh
bash ~/.vim/vim_setting/script/YouCompleteme.sh
```
### 三、常见问题
1. apt lock  
```
1. 终端输入 ps  aux ，列出进程。找到含有apt-get的进程，直接sudo kill PID.
2. 强制解锁
    sudo rm /var/cache/apt/archives/lock
    sudo rm /var/lib/dpkg/lock
```
2. update  404 not found  
```
sudo apt clean
sudo apt update
sudo apt upgrade
```
