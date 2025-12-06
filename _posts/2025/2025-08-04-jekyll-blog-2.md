---
title: Jekyll博客搭建(二) | 远程仓库配置
author: 0x_716
date: 2025-08-04 6:30:00 +0800
categories: [blog]
tags: [blog]
pin: true
math: true
mermaid: true
image:
  path: assets/cover/blog-2.png
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
---



## 仓库创建

使用Chirpy主题作者创建的[Chirpy Starter ](https://github.com/cotes2020/chirpy-starter)模板创建一个新的 GitHub 仓库存储blog内容。

- 这个 tempalte 包含了blog所需的所有内容（Jekyll、Chirpy theme、GitHub Action 等）

- Use this template -> Create a new repository

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206203951458.png)

仓库名称为`USERNAME.github.io`，`USERNAME`使用自己的 GitHub 用户名

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206204044263.png)

## clone到本地

```
git clone https://github.com/ffkkaq/ffkkaq.github.io.git my-blog
cd my-blog
bundle install  #安装Jekyll依赖项
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206204127612.png)

```
bundle exec jekyll serve   #预览Jekyll网站
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206204203965.png)

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206204303322.png)

## GitHub Pages

- 打开的 GitHub 仓库`Setting`
- 选择`Page`选项栏
- 将`Build and Deploy` 修改为`Github Action`

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206204337706.png)

