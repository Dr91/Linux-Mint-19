# Linux mint 安装步骤
## 制作U盘启动盘
### 下载iso文件
官网下载地址:https://www.linuxmint.com/download.php
### 下载rufus-3.5软件 制作U盘启动盘。
官网下载地址:https://rufus.ie/
## 安装Linux mint
电脑重启从U盘进入系统，直接选择 Install linux mint 快捷方式进行安装系统
###### 安装时注意：
1. 不要联网：如果联网安装是会下载语言包，巨慢。
2. 选择英文：安装时选择英文。到时候自己下载语言包就可以。如果选择中文的话会有字体问题。
## 换国内源
1. 进入 Menu->Software Scoures
2. 先点击Update the cache 更新 源列表 然后就可以选择源了(根据网速选择快的源)。
```
$ sudo apt update $ sudo apt upgrade
```
## 安装语言包
```
$ sudo apt-get install language-pack-zh-hans language-pack-gnome-zh-hans libreoffice-l10n-zh-cn thunderbird-locale-zh-hans firefox-locale-zh-hans
```
进入 Menu->Language设置语言
## 安装搜狗输入法
1. 搜狗官网下载linux版的.deb文件直接双击就好了，重新启动
2. 打开Fcitx配置
## 安装多媒体插件
```
$ sudo apt-get install mint-meta-codecs
```
## 清洁系统
```
将已经删除了的软件包的.deb安装文件从硬盘中删除： 
$ sudo apt-get autoclean 
删除包缓存中的所有包： 
$ sudo apt-get clean 
删除为了满足其他软件包的依赖而安装的，但现在不再需要的软件包： 
$ sudo apt-get autoremove 
删除已安装的软件包（保留配置文件）:
$ sudo apt-get --purge remove 软件包名称
```
