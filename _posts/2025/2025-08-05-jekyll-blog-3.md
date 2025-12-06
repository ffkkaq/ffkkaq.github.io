---
title: Jekyll博客搭建(三) | 个性化配置
author: 0x_716
date: 2025-08-05 21:40:00 +0800
categories: [blog]
tags: [blog]
pin: true
math: true
mermaid: true
image:
  path: assets/cover/blog-3.png
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
---


## 头像

将头像图标放在 `assets/img/favicons/` 目录中后进行配置准备大小为 512x512 或更大的方形图片（PNG、JPG 或 SVG），在转换网站 [**Real Favicon Generator**](https://realfavicongenerator.net/) ， 点击Pick your favicon image 按钮上传图片文件。


一直下一步，网页将显示所有使用方案预览效果，拉到最下面，直接点击下一步,点击Download下载。

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206205533566.png)

下载生成的压缩包，解压后删除`site.webmanifest`文件，复制剩余的图片文件（`.PNG` 和 `.ICO`）到 `assets/img/favicons/` 目录中。如果Jekyll 网站没有此目录，创建一个即可

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206205622256.png)

在_config.yml文件中修改**avatar**选项

```
avatar: "/assets/img/favicons/web-app-manifest-512x512.png"
```

## 其他设置

这里主要相关的两个文件为:`/_config.yml` 和`/_data/contact.yml` 

设置_config.yml文件中的关键字段来个性化配置修改：

- **title**：主标题
- **tagline**：标签描述
- **description**：网站描述

我的主要设置如下：

```yml
theme: jekyll-theme-chirpy
lang: zh-CN
timezone: Asia/Shanghai
tagline: 0x_716 blog # it will display as the subtitle
url: "https://ffkkaq.github.io"
github:
  username: ffkkaq # change to your GitHub username
```

>这里设置的`title`以及`description`没有设置的原因是发现了主题的一些小Bug，不知为何，将`0x716`识别为十六进制的数字，显示为`1814`，如下图，且设置语言为中文后，`description`会直接不显示。
{: .prompt-warning }

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206205707961.png)

设置`/_data/contact.yml` 文件来个性化左侧边栏底部的图标

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206205758226.png)

这里注释掉对应的项就不会显示了，如果需要新增，则在红框中的图标网站搜索相应图标后添加对应的项即可。



