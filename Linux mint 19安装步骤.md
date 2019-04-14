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
```
路径：Menu->Software Scoures
先点击Update the cache 更新 源列表 然后就可以选择源了。
可以根据网速选择快的源
```
执行 sudo apt update 和 sudo apt upgrade 命令了，进行更新。




