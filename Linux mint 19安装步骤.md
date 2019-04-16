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
## 更新apt-get 
```
/etc/apt/sources.list 和 /etc/apt/sources.list.d 中列出的源的地址,这样才能获取到最新的软件包
$ sudo apt update 
升级已安装的所有软件包，升级的版本就是更新的源地址里的版本，因此，在执行 upgrade 之前一定要执行 update
$ sudo apt upgrade
```
## 安装语言包
```
$ sudo apt-get install language-pack-zh-hans language-pack-gnome-zh-hans libreoffice-l10n-zh-cn thunderbird-locale-zh-hans firefox-locale-zh-hans
```
进入 Menu->Language设置语言

## 安装多媒体插件
```
$ sudo apt-get install mint-meta-codecs
```
## 清洁系统（卸载apt-get）
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
# 补充：sudo apt-get常用命令
## 安装
```
1.
$ sudo apt-get install -f
参数为–fix-broken的简写形式，可以在man apt-get 中搜索-f参数查询到其帮助信息
-f参数的主要作用是是修复依赖关系（depends），假如用户的系统上有某个package不满足依赖条件，这个命令就会自动修复，安装程序包所依赖的包。
2.
$ sudo apt-get install 软件包名称：
```
##一般安装/卸载步骤
```
eg:安装atom时：
1.一般安装软件前需要更新依赖库
$ sudo add-apt-repository ppa:webupd8team/atom
2.再更新源地址
$ sudo apt-get update
3.最后安装该软件
$ sudo apt-get install atom

一般卸载步骤
1.先卸载软件
$sudo apt-get remove atom
2.再卸载依赖库
$sudo add-apt-repository --remove ppa:webupd8team/atom
3.再使用autoremove
$sudo apt-get autoremove
```

