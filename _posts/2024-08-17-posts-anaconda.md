---
title: "在Anaconda里安装pypi的package"
layout: blog
excerpt: "如何在Anaconda里安装pypi的packag"
read_time: true
comments: true
share: true
# author_profile: true
classes: wide
categories:
  - 欧耶之AI
tags:
  - Anaconda
  - pypi
---

Anaconda是一个用于科学计算的Python发行版，它使得安装和管理Python包变得更加容易。它本身包含了很多常用的package。而PyPi（Python Package Index）是一个用于Python包管理的软件仓库。它包含了数千个Python软件包和模块，可以满足各种不同的需求。通过PyPi，我们可以方便地查找、安装、升级和删除各种Python软件包。下面来介绍在Anaconda的运行环境下安装本身没有的在pypi里的包。

1. 首先打开anaconda命令行。
2. 然后输入：`conda install -c conda-forge package_name`。这里package_name是你想要安装的package。结束。
3. 升级package：`conda update package_name`。
4. 删除package: `conda remove package_name`。



