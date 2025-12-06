---
title: Jekyll博客搭建(五) | 图床搭建
author: 0x_716
date: 2025-08-08 22:40:00 +0800
categories: [blog]
tags: [blog]
pin: true
math: true
mermaid: true
image:
  path: assets/cover/blog-5.png
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
---

使用github作为图床的优势在于免费、稳定，适合个人blog。PicGo图床上传工具用起来也比较方便快捷

Github官方仓库下载最新版[PicGo](https://github.com/Molunerfinn/PicGo),选择对应版本

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206211814226.png)

创建一个仓库，用来存放上传的图片

- 设定仓库名：Username/Repository
- 设定Token：Github->Setting->Developer setting 
- 设定存储路径：在创建的仓库下创建文件夹即可

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206212024839.png)

Token获取方式如下图，这里选择第一种Token,可以精确到某个具体的仓库，而不是第二种账户级别的授权，相比较起来，第一种更安全。

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206212053581.png)

Token的时间期限，根据个人使用习惯进行选择

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206212116691.png)

选择仅图床这个仓库的权限

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206212153562.png)


这里的权限选择为`Contents`的读写权限

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206212226081.png)

打开以下几个设置后，进行图片的上传

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206212310370.png)