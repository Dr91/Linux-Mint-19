# 彻底卸载LibreOffice方法
```
对所有基于 Debian 的发行版（Debian、Ubuntu、Kubuntu、Xubuntu、*buntu、Sidux 等）：

sudo apt-get purge libreoffice?

或

sudo aptitude purge libreoffice?

不要漏掉通配符“?”，否则无法清除/卸载全部 LibreOffice 软件包

或者

sudo apt-get remove --purge libreoffice*
```
