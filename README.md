# article
# 1. 安装和卸载sublime

> 安装sublime

找到软件包,一般是 .deb结尾的文件, 然后 cd 到 安装包所在的文件夹,输入以下代码

```
sudo dpkg -i 压缩包的名字.deb

# 如果在安装过程中出现了问题,就输入下面的代码修复
sudo apt-get install -f
```

卸载sublime

```
# 完全卸载命令
sudo dpkg -r sublime-text
```

如果还是不能完全卸载,就输入如下的命令

```
sudo apt-get remove sublime-text-installer

# 在终端输入下面命令，删除配置文件 其中$USER是你自己的系统用户名，回车
sudo rm -rf /home/$USER/.config/sublime-text-3/

# 在终端输入下面命令，查找系统中其他与Sublime Text3相关的文件及路径
sudo find / -name sublime*

# 重复在终端输入删除命令，删除其他与Sublime Text3相关的全部文件,文件路径和名称 为上面find命令查找到的文件
sudo rm -r /home/long/.local/share/Trash/info/sublime-text_build-3083_i386.deb.trashinfo

# 重复rm  删除所有有关sublime的文件,直到完全卸载完成
```
