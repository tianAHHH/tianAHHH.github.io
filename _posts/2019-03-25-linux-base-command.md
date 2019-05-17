---
title: linux基本命令
layout: post
categories: linux
tags: linux, shell
excerpt: linux基本命令
---
# linux基本命令

linux的命令很多，对想学习的朋友来说，无疑很头痛，那么先从这些常用的开始吧

## 列出文件

```shell
    ls    显示非隐藏文件
    ls -a    显示所有文件
    dir
```

## 更换目录

```shell
    cd
    cd /    进入根目录
```

## 创建目录

```shell
    mkdir
```

## 当前目录

```shell
    pwd
```

## 删除

```shell
    rm [文件名]
    rm -rf 强制删除
    rm -r 删除该文件夹及下面的所有文件
```

## 复制

```shell
    cp [当前] [变更]
    当复制的文件在当前目录时，名字会变更
```

## 移动

```shell
    mv [当前] [变更]
    可以使用该方法更改文件名
```

## 重命名

```shell
    rename [旧类型] [新类型] [筛选]
```

## 创建文件

```shell
> filename
touch filename 创建二进制文件
vi filename 创建带文件格式的文件
```

## 解压缩

```shell
    tar [选项] 文件名 文件/文件夹    压缩文件
        选项：-cf  -rf  -uf
        f是表示文件，c是表示产生新的包，r是表示增加文件，u是表示更新文件

    tar [选项] 文件名    解压文件
        选项：-tf  -xf
        t是列出文件，x是解包

    调用gzip    在选项中添加参数：-z    
        例子: tar -czf all.tar.gz *.jpg
              tar -xzf all.tar.gz

    调用bzip2    在选项中添加参数：-j
        例子: tar -cjf all.tar.bz2 *.jpg
              tar -xjf all.tar.bz2

    解压缩zip
        zip all.zip *.jpg    压缩文件
        zip -r temp.zip temp    压缩文件夹
        unzip all.zip    解压

    rar    linux下的rar需要安装RAR for Linux，但是需要付费
```

## 参考

```shell
    man "commond"
```

想要学习linux最有用的指令

## 查找

```shell
    find -iname [目录] 文件名    查找指定目录下的文件
```

## 显示进程

```shell
    ps
    ps -a    显示所有进程
```

## 筛选

```shell
    [其他命令] | grep [筛选内容]
    例：
        ps -a | grep [shell]
```

## 显示内容

```shell
    cat    不分页查看
    cat more    分页查看
    echo message
```

## 关机

```shell
    halt
    shutdown ［选项］ ［时间/now］ ［警告信息］
    - k 并不真正关机，而只是发出警告信息给所有用户。
    - r 关机后立即重新启动。
    - h 关机后不重新启动。
    - f 快速关机，重启动时跳过fsck。
    - n 快速关机，不经过init程序。
    - c 取消一个已经运行的shutdown。
```

## 重启

```shell
    reboot
```

## 显示系统运行时长

```shell
    uptime
```

## 修改密码

```shell
    passwd
```

## 管理员

```shell
    su ［选项］ ［? ］ ［使用者帐号］    切换至管理员身份
        切换需要输入管理员密码
    sudo command    以管理员权限执行命令
        使用需要输入密码
```

## 日历

```shell
    cal  ［选项］ ［月 ［年］］
    date ［选项］ 显示时间格式（以+开头，后面接格式）
```

## 清屏

```shell
    clear
```

export 定义

```shell
    export LC_ALL=#定义一个变量LC_ALL并且设置为空NULL
    export LANG=zh_CN.gb2312#定义一个变量LANG的值是zh_CN.gb2312 
    export http_proxy="http://192.168.1.2:80"#定义http代理服务器
```