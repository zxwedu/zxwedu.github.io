---
title: 'Install Caffe on ubuntu'
date: 2016-04-14
permalink: /posts/2016/04/install-caffe/
tags:
  - ubuntu
  - Caffe
---

【转载】Caffe + Ubuntu 15.04 + CUDA 7.5 新手安装配置指南

<p>为了方便地找到欧新宇老师配置caffe的博客，故转载欧老师的博客到自己的博客下。感谢欧老师的辛勤工作。</p>

<p>参考自以下连接：</p>
      <p><a href="http://ouxinyu.github.io/Blogs/20151108001.html">
	  Caffe + Ubuntu 15.04 + CUDA 7.5 新手安装配置指南</a></p>
	  

<p><b>（1）nVidia CUDA Toolkit的安装（*.deb方法）</b></p>

<p>一、CUDA Repository<br>
获取CUDA安装包,安装包请自行去NVidia官网下载。（https://developer.nvidia.com/cuda-downloads）<br>
$ sudo dpkg -i cuda-repo-ubuntu1504-7-5-local_7.5-18_amd64<br>
$ sudo apt-get update<br>
二、CUDA Toolkit<br>
$ sudo apt-get install -y cuda</p>


<p><b>（2）Caffe-Master的安装和测试</b></p>
<p>具体参考下图：</p>
<img src='./Blogs/img/caffe1.jpg'/>
<img src='./Blogs/img/caffe2.jpg'/>
<img src='./Blogs/img/caffe3.jpg'/>
<img src='./Blogs/img/caffe4.jpg'/>

<p>本文只截取了部分安装过程，更具体的操作，请参考欧老师的博客。<a href="http://ouxinyu.github.io/Blogs/20151108001.html">
	  Caffe + Ubuntu 15.04 + CUDA 7.5 新手安装配置指南</a></p>
	  
<p><b> caffe安装个人心得：</b></p>
	<p>1、ubuntu14.04.3系统，安装cuda7.5可以正常使用。但是连接KVM的话，使用cuda7.5的驱动，分辨率会不正常。</p>
	<p>2、连接kvm的nvidia显卡驱动版本为352.63时，分辨率正常。</p>
	<p>3、ubuntu 14.04.1系统，配合cuda7.0和cudnnV4，caffe可以正常使用。而且安装的显卡驱动版本也为352.63，kvm也可正常使用。</p>
	<p>4、安装caffe下的所有软件，一定要在全英文的路径下，路径中不要包含中文，特别是安装opencv的时候。</p>
	<p>5、实践证明的可使用组合：
	<br>硬件：titanX显卡，无单独显卡；Intel core i5-4590CPU，4核；32G内存；
	<br>ubuntu系统14.04.1，64位操作系统
	<br>cuda7.0；cudnnV4；opencv3.1.0；parallel studio 2013；google golg-0.3.3；MATLAB 2014b
	</p>
