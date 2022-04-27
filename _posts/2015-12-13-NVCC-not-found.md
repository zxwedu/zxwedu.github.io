---
title: 'NVCC not Found in ubuntu'
date: 2015-12-13
permalink: /posts/2015/12/nvcc-not-found/
tags:
  - ubuntu
  - NVCC
---

<p>参考自<a href="https://devtalk.nvidia.com/default/topic/695011/matlab-not-seeing-nvcc/">https://devtalk.nvidia.com/default/topic/695011/matlab-not-seeing-nvcc/</a></p>

<p>在matlab命令行中输入 </p>

<p>edit startup</p>

<p>It will open or create the file startup.m. Add the setenv line to the file, next time you restart Matlab the command
will be automatically executed.</p>

<p>在打开的startup.m文件中，输入 setenv('BASH_ENV','/etc/profile'); </p>
<p>/etc/profile中，必须有export的nvcc的环境变量，例如 export PAHT=/usr/local/cuda-7.0/bin:$PATH</p> 
<p>export LD_LIBRARY_PATH=/usr/local/cuda-7.0/lib64:$LD_LIBRARY_PATH</p>