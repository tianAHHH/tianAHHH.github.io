---
title: create website
layout: post
categories: web
tags: web
excerpt: create website
---

# 搭建个人博客网站

## 一、完整建站流程

### 1、需求分析

**搭建博客**

### 2、注册域名

阿里云、腾讯云、七牛云等等

### 3、购买服务器/主机

阿里云、腾讯云

### 4、域名备案

备案码、地方备案

### 5、网站源码上传

在服务器中上传项目并搭建好服务

### 6、域名解析

一般购买了域名后会有免费版的解析，要求高可以付费解析

## 二、实施流程

**炒鸡省钱建博客站方案**
通过`github.io`或者`gitee.io`搭建静态网页，使用域名解析至对应的地址，这里以github.io为例开始建站

### 1、注册Github

[Github官网](htttps://github.com)
例如：`hn-failte`

### 2、创建github.io项目

创建一个项目，项目的名称为`用户名+github.io`
例如：`hn-failte.github.io`

### 3、上传源码到项目

#### 测试

可以先只放一个`index.html`文件在仓库中

#### 项目处理：

* (1)在网站上直接上传文件
* (2)使用git推送到远程仓库（拓展）
    git手册：https://gitee.com/progit/

### 4、pages服务

要想在`广域网`访问站点，需要开启设置中的`pages`服务

![Alt](https://hn-failte.github.io/assets/posts/web-create-website-1.png#pic_center =30x30)

自定义域名默认为空
开启服务后，可以在`广域网`通过`用户名.github.io`访问你的站点，即之前放的index.html
例如：`hn-failte.github.io`

### 5、源码编写

#### (1)[`jekyll(基于Ruby`)](https://github.com/jekyll/jekyll)

##### 使用此方案，之后写的博客都需要按照框架的要求使用`markdown`语言编写博客，且文件名也有一定的要求，如：

![Alt](https://hn-failte.github.io/assets/posts/web-create-website-2.png#pic_center =30x30)

##### 不想学该框架，如何快速搭建：

###### [下载我的源码](https://github.com/hn-failte/hn-failte.github.io.git)

**修改文件**，去除一切带个性化字眼的文字

* _config.yml  //该文件大部分要修改

* assets/res  //图片资源，替换要改的
bg.png  //左上角背景图，不要太大，推荐320x180
failte.png  //左下角微信图片，可更名，引用同步更改即可
favicon.ico  //网页ico图
logo.png    //大头像
user.png    //小头像
wechat图标不要动，其他的图都可以删除

* _post文件夹用来放博客文章

* _layout文件夹
post.html中可以修改侧边栏，不推荐大改

* _includes文件夹
footer.html可修改页脚
contact.html可修改邮箱
about.html修改其他信息

至此，修改就完成了，将代码上传到`github`仓库，pages服务开启的情况下`github`会自动更新站点，此时就完成了`github`博客的搭建。浏览器中输入`用户名.github.io`查看效果。[点击查看我的博客效果](hn-failte.github.io)

##### `Markdown`编辑器:
`Typora`、`Atom`、`Sublime`、`VSCode`、`MarkdownPad`、`MaHua`、各大博客网站在线编辑器

##### 博客网站：

* [博客园](http://www.cnblogs.com/)
* [csdn](https://blog.csdn.net/)
* [简书](https://www.jianshu.com/)

#### (2)其他博客框架方案

#### (3)其他方案

* 使用`Bootstrap`或者自己写模板等。（方案）
* 自主性高，但是会造成一个问题，若以`markdown`文件作为博客文件，浏览器无法正常解析，只能得到`txt`的效果，若以`html`的样式写，工作量大且显得不专业。（专业性）
* 若是网站不是用来写博客，完全可以自己随意写。（作用）

### 6、域名处理

* 我希望别人通过我的域名访问，而不是`github`的那一长串的域名。

#### 1、购买域名

选一个学习用的`域名`，价格很廉价

#### 2、解析

* (1)在域名商的控制台添加域名解析。
![Alt](https://hn-failte.github.io/assets/posts/web-create-website-3.png#pic_center =30x30)

以我注册的域名为例，failte.cn是顶级域名，上图中blog开头的解析属于二级域名的解析，CNAME意在指向另一域名，记录值是上边创建的github.io地址，例如hn-failte.github.io。

* (2)github.io在设置内填写设置的域名，例如blogs.failte.cn。

#### 3、调试访问

打开浏览器，输入解析地址，例如blogs.failte.cn。

## 收尾分析

我们最终的目的是学习建站过程以及写博客，那不妨先总结下

### 优点：

* 终于 **`无需备案`** 了
* **`广域网`**
* 巧妙跳过了服务器/主机的购买， **`省成本`**
* 简单， **`不需要搭建后台`**
* 找工作时， **`面试加分`**

### 缺点：

* 没有后台支持，使用`pages`只能搭建`静态网站`
* 当然，获取使用跨域资源是完全可以的

### 解决方案：

第三方工作室`主机`，只用来学习的话很好用，这里就不说了，有打广告的嫌疑