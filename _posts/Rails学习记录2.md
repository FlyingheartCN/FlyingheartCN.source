---
title: Rails学习记录2
date: 2018-02-04 10:53:14
tags: 
    - Ruby
    - Rails
    - 编程
---

### 编辑器配置：
在Windows上写代码，通过sftp同步到Linux上，Linux上运行rails console，通过ssh进行调试
编辑器为VSCode，安装扩展ftp-sync、Ruby、Ruby on Rails、Simple Ruby ERB
ftp-sync.json配置如下
```
{
    "remotePath": "/home/ruby/rails/blog",
    "host": "10.0.0.12",
    "username": "username",
    "password": "password",
    "port": 22,
    "protocol": "sftp",
    "uploadOnSave": true,
    "passive": false,
    "debug": false,
    "privateKeyPath": null,
    "passphrase": null,
    "ignore": [
        "\\.vscode",
        "\\.DS_Store"
    ],
    "generatedFiles": {
        "uploadOnSave": false,
        "extensionsToInclude": [],
        "path": ""
    }
}
```

### 远程调试：

在Windows上安装openssh、git，并且把bin加入PATH中，连接服务器的时候，命令为
```
ssh -L 3000:10.0.0.12:3000 ruby@10.0.0.12
```
这样就把虚拟机的3000端口映射到本地了，我的VMWare不知为何不能直接访问3000端口，所以只能这样解决
rails console则和Linux上开发没有区别