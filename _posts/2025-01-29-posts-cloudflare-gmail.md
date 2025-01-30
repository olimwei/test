---
title: "用Cloudflare和Gmail搭配收发专属域名邮件"
layout: blog
excerpt: "用Cloudflare和Gmail搭配收发专属域名邮件"
read_time: true
comments: true
share: true
# author_profile: true
classes: wide
categories:
  - 欧耶之AI
tags:
  - cloudflae
  - Gmail
---

如有个专属的网站域名（yoursite.com)，可以使用cloudflare的邮件转发功能，把发往专属域名邮箱（xx@yoursite.com)的邮件转发到Gmail免费邮箱里，在gmail里经过设置，也可以通过gmail以xx@yoursite.com的名义发送邮件。这样就可以在gmail里统一管理自己拥有的专属域名邮件了。具体步骤如下：

### 准备条件
1. 注册一个cloudflare账户
2. 在cloudflare里添加专属域名(yoursite.com)
3. 在电子邮件>电子邮件路由那里开通邮件路由

### 接收邮件
在cloudflare的邮件路由那里创建专属域名的电子邮箱，转发到指定的Gmail地址。如果第一次创建，会gmail收到验证邮件，确认后点击确认，cloudflare会自动添加相应的DNS记录。

随后所有发往专属域名邮箱(xx@yoursite.com)的邮件会全部转发到指定的Gmail地址。

### 发送邮件
因cloudflare只转发专属域名邮箱接收到的邮件，暂不支持发送邮件，这里需要到gmail里进行一番设置，达到可以通过gmail以专属域名邮箱的名义发送或回复收到的邮件。

1. 首先到https://myaccount.google.com/apppasswords生成一个密码。
2. 打开gmail的设置，在accounts and import下面的“Send mail as"里点击“Add another email address",填写专属域名邮箱相应信息。
3. 点击下一步后 在SMPT那里填写 smpt.gmail.com, port端口默认，username填写gmail账号，密码用第一步生成的密码。
4. 收到验证码确认

至此，专属域名邮箱的收发全部都可以在指定gmail里完成。
