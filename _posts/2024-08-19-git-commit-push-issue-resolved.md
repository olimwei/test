---
title: "出现了一个git commit push去master的问题"
layout: blog
excerpt: "出现了一个git commit push去master的问题"
read_time: true
comments: true
share: true
# author_profile: true
classes: wide
categories:
  - 欧耶之AI
tags:
  - git
  - issue
---

周末把上周跟踪的股票每日复盘汇总成一个post，忘记上传服务器，今天想起来，在vs code里赶紧常规点击commit and push，不曾想居然出现了问题。`RPC failed; HTTP 400 curl 22 The requested URL returned error: 400`。傻眼了，这哪里是我能知道解决的事啊。。。马上采取了最原始暴力的办法，把新加的文件易到另外一个目录，然后把整个项目的folder删除，重新从服务器clone下载到本地电脑，再把新文件放回到该在的地方，再次重复以往的动作。。。还是不行。。。

我是“万事不决问谷歌”时代的人，万能的互联网再次帮我提供了解决方法，如下：
打开terminal，在项目目录下输入这个命令`git config http.postBuffer 524288000`。搞定！

对我这样不知其然也不知其所以然的人，谷歌加无脑听从指挥就好了。别人也就一行代码的事，要让我知道为什么，那是几个月也搞不明白的。😄

赶紧记录一下，下次遇到同样的问题，也好到这里来直接找到代码copy&paste。