---
title: "在git提交的时候去掉隐藏文件DSStore"
layout: blog
excerpt: ".DS_Store是文件访问时自动创建的隐藏文件，在提交git的时候会带来一些问题。可以这样处理："
read_time: true
comments: true
share: true
# author_profile: true
classes: wide
categories:
  - 欧耶之AI
#tags:
#  - 
#  - 
---

.DS_Store是文件访问时自动创建的隐藏文件，在提交git的时候会带来一些问题。可以这样处理：

先把 GitLab 中的这个文件处理掉：

1. 先把远程库的代码拉下来，看到这个隐藏文件在不在。
2. 用 `git rm -r --cached .DS_Store`和`git commit -m 'delete .DS_Store'`去除。
3. 在 gitignore 中设置忽略。*/.DS_Store

还可以做一个全局设置，一劳永逸。方法如下：
1. 创建一个全局文件 ～/.gitignore_global
2. 把下面内容写入：`echo ".DS_Store" >> ～/.gitignore_global`, `echo "._.DS_Store" >> ～/.gitignore_global`, ``echo "**/.DS_Store" >> ～/.gitignore_global`, `echo "**/._.DS_Store" >> ～/.gitignore_global`.
3. 再全局设置一下：`git config --global core.excludesfile ~/.gitignore_global`