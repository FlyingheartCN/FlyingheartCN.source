---
title: 使用GPG加密你的电子邮件
date: 2018-05-19 22:45:17
tags: 
---
首先，你需要先安装GPG和Thunderbird电子邮件客户端
<!-- more -->
首先，在Thunderbird上安装Enigmail扩展
安装好之后，打开Enigmail的选项，把gpg的目录设置到(Windows下，Linux下应该可以自动探测)
```
C:\Program Files (x86)\GnuPG\bin\gpg.exe
```
打开kleopatra，生成一个你的密钥对，把公钥上传到服务器上，例如
```
pgp.mit.edu
keyserver.ubuntu.com
```
用你的私钥给别人的公钥认证后，给此人发送邮件的时候选上它，并用自己的私钥签名即可