---
title: "开始安装学习python"
layout: blog
excerpt: "开始安装学习python"
read_time: true
comments: true
share: true
# author_profile: true
classes: wide
categories:
  - 欧耶之AI
tags:
  - Python
---

先是一些准备工作。

## Brew在Mac上安装
1. 先check是否安装，查版本：`python3 --version`. 
2. brew安装：`brew install python3`

## 在虚拟环境中工作
### 方法一：用自带的venv命令
1. 在工作目录下建立 virtualenvirament: `python -m venv venv`
2. 激活虚拟环境：`source ~/python project/venv/bin/activate`
3. deactivate直接输入： `deactivate`

### 方法二：安装poetry (选择用这个👌)
`curl -sSL https://install.python-poetry.org | python3 -` 点击[poetry](https://python.land/virtual-environments/python-poetry)了解情况。

## 选择了用两种工具写python
### 在Jupyter notebook/lab写python
在terminal打开 `$ jupyter lab` （取代`$ jupyter notebook`），输入后打开网页编辑模式。。。在这里可以选创建文件的格式和环境 .md, ,ipynb, .py等文件格式。
Jupyter是个在数据分析和机器学习领域广泛使用。

安装为 Jupyter 提供 IPython 内核的ipykernel `pip install --user ipykernel`。。。。用`python -m ipykernel install --user --name=myenv`安装新虚拟环境。。。用`jupyter kernelspec list`查看虚拟环境内核list。。。。。`jupyter kernelspec uninstall myenv`命令删除不要的内核。

### 用VS code来写python
VS code作为跨平台支持各种语言的editor，可以通过extension添加很多扩展功能。可以加python extension来写python，还可以加Jupyter extension来使用。。。这样包括写markdown文件也可以一并在这里写了。

这两种工具可以根据具体使用要求选择使用。

## 当前的学习目标
* 作为程序语言的Python基本语法
* 数据分析和视觉化方向，比如股票分析。用到Numpy, Pandas, Matlibplot, Yfinanc等。

## 一些资源 （都是网上游荡找来的随手放在这里）
* [Python在W3学校的tutorial](https://www.w3schools.com/python/)
* [Learn Python](https://www.learnpython.org/)
* [Python官方文档](https://docs.python.org/3/tutorial/index.html)当然这个python官方文档是最枯燥也最重要的地方
* [一个提供Tex equation editor的网站](https://atomurl.net/math/)

## 网上游荡发现的一些东西（放在这里，也许以后有兴趣翻回来看看）
- 一个叫 [Sphinx](https://www.sphinx-doc.org/en/master/) 的Python原始文档生成软件（工具），简单浏览了一下，写文档看上去很干净整洁，很不错的样子。应该原生态支持python语言，也支持markdown。