# snap简介 
snap是一种全新的软件包管理方式,它类似一个容器包含一个应用程序所有的文件和库,各个应用程序之间完全独立.
## 优势
它解决了软件包的依赖问题,使应用程序更容易管理.
## 劣势
占用更多的磁盘空间.
## snap的安装包
扩展名是.snap,类似于一个容器,它包含一个应用程序需要用到的所有文件和库（snap包包含一个私有的root文件系统，里面包含了依赖的软件包）.它们会被安装到单独的目录;各个应用程序之间相互隔离.
snap软件包一般安装在/snap目录下

# snap安装
```
sudo apt-get install snapd
sudo apt-get install snapcraft
```
## 常用的命令
###### 列出已经安装的snap包
`sudo snap list`
###### 搜索要安装的snap包
`sudo snap find <text to search>`
###### 安装一个snap包
`sudo snap install <snap name>`
###### 更新一个snap包，如果你后面不加包的名字的话那就是更新所有的snap包
`sudo snap refresh <snap name>`
###### 把一个包还原到以前安装的版本
`sudo snap revert <snap name>`
###### 删除一个snap包
`sudo snap remove <snap name>`
# 常用软件
```
# clion
sudo snap install clion
# pycharm
sudo snap install pycharm
# 网易云音乐
sudo snap install netease-music --devmode --beta
# 微信
sudo snap install electronic-wechat deepin-music

```

