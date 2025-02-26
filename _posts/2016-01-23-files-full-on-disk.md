---
title: 'Files full on disk'
date: 2016-01-23
permalink: /posts/2016/01/files-full-on-disk/
tags:
  - ubuntu
  - not start
---

ubuntu系统磁盘已满，导致系统无法启动

<p>1.因为无法进入ubuntu系统桌面，所以要尝试进入tty1-tty6命令控制台，使用命令ctrl+alt+f1~f6 </p>

<p>2.进入tty1-tty6界面后，登录自己的系统。输入用户名，密码即可</p>

<p>3.首先输入命令，df -l 查看自己的磁盘是否确实已满。如果已满，磁盘会显示使用率100%。</p>

<p>4.查看系统中的大文件有哪些。</p>
<p>查找磁盘上大于20MB的文件</p>

<p>find / -size +20000k -exec ls -lh {} \;  </p>
<p>查找磁盘上大于400MB的文件，直接删除，一般都是日志文件</p>

<p>find / -size +400000k -exec rm -rf {} \;  </p>
<p>具体可以参考<a href="http://www.2cto.com/os/201412/358960.html">linux下查找大文件的方法</a></p>

<p>5.使用命令行命令删除部分不需要的大文件。命令如下：sudo rm -R 待删除的文件名 </p>
<p>6.使用reboot命令重启电脑即可。</p> 