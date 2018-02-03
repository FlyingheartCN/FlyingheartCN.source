---
title: Rails学习记录1
date: 2018-02-02 18:40:21
tags:     
    - Ruby
    - Rails
    - 编程
---
<!-- more -->

### 安装：
我的电脑是Windows系统，所以为了方便我在VMware中安装了虚拟机，系统是CentOS7，保持最新

安装rvm：
```
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
curl -L https://raw.githubusercontent.com/wayneeseguin/rvm/master/binscripts/rvm-installer | bash -s stable
source ~/.rvm/scripts/rvm
echo "ruby_url=https://cache.ruby-china.org/pub/ruby" > ~/.rvm/user/db
```
结果：
```
[ruby@localhost ~]# rvm -v
rvm 1.29.3 (latest) by Michal Papis, Piotr Kuczynski, Wayne E. Seguin [https://rvm.io]
```
安装ruby 2.5.0：
```
rvm requirements
rvm install 2.5.0
rvm use 2.5.0 --default
```
结果：
```
[ruby@localhost ~]# ruby -v
ruby 2.5.0p0 (2017-12-25 revision 61468) [x86_64-linux]
[ruby@localhost ~]# gem -v
2.7.3
```
安装rails：
```
gem sources --add https://gems.ruby-china.org/ --remove https://rubygems.org/
gem install bundler
gem install rails
```
结果：
```
[ruby@localhost ~]# rails -v
Rails 5.1.4
```
好了，安装已经完成了，可以说安装的步骤很简单~~比Gitlab不知道简单到哪里去了~~