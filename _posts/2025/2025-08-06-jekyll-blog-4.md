---
title: Jekyll博客搭建(四) | 内容撰写
author: 0x_716
date: 2025-08-06 06:40:00 +0800
categories: [blog]
tags: [blog]
pin: true
math: true
mermaid: true
image:
  path: assets/cover/blog-4.png
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
---


## 元数据

所有写的blog内容全部在在 `_posts/` 文件夹内，为了方便管理，这里建议按照年份创建子文件夹，blog的命名方式为`YYYY-MM-DD-TITLE.MD`这里建议命名为英文，这样文章链接更短更易识。

```
_posts/2025/2025-12-05-jekyll-blog-1.md
```

Jekyll 中的每篇blog都以**front matter**开头，一个被 `---` 包围的YAML内容，，包含该帖子的元数据。这些元数据指导了 Jekyll 如何处理和显示内容。

```
---
title: Jekyll博客搭建(一)| 本地环境搭建
author: 0x_716
date: 2025-12-04 18:33:00 +0800
categories: [blog]
tags: [blog]
pin: true
math: true
mermaid: true
image:
  path: assets/cover/blog-1.png
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
  alt: Responsive rendering of Chirpy theme on multiple devices.
---
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206210227288.png)
## 分类

Chirpy支持多级分类,下例体现在左侧边栏中的分类中如图所示

```
categories: [Blogging,Demo]
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206210252484.png)
## 目录开关

默认情况下，目录显示在右侧面板上，如果想全局关闭，可以进入 `_config.yml`，把变量 `toc` 的值设为 `false`。如果想关闭某篇帖子的目录，可以在帖子的**front matter**中添加以下内容：

```
---
toc: false
---
```

## 图片图注

在图片的下一行加上如下所示，这样它就会成为图注，并出现在图片底部：

```
![img-description](/path/to/image)
_Image Caption_
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206210325218.png)
## 图片大小

通过宽度和高度来设置图片大小

```
![Desktop View](/assets/img/sample/mockup.png){: width="700" height="400" }
```

从 *Chirpy v5.0.0* 开始，`height` 和 `width` 支持缩写（`height` → `h，width` → `w`）。 以下示例具有与上述相同的效果：

```
![Desktop View](/assets/img/sample/mockup.png){: w="700" h="400" }
```

## 图片位置

四种图片的展示形式，`默认模式`、`左对齐`、`向左漂浮`、`向右漂浮`。需要注意的是只有默认模式可以加图注

**默认模式：默认居中显示**，语法与显示效果如下

```
![Desktop View](/assets/img/sample/mockup.png){: width="700" height="400" }
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206210446774.png)

**左对齐：语法与显示效果如下**

```
![Desktop View](/posts/20190808/mockup.png){: width="972" height="589" .w-75 .normal}
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206210534162.png)
**向左浮动：语法与显示效果如下**

```
![Desktop View](/posts/20190808/mockup.png){: width="972" height="589" .w-50 .left}
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206210610321.png)
**向右浮动：语法与显示效果如下**

```
![Desktop View](/posts/20190808/mockup.png){: width="972" height="589" .w-50 .right}
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206210652761.png)
## 四种列表样式

四种列表样式，`Ordered list`、`Unordered list`、`ToDo list`、`Description list`四种

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206210717852.png)

## 四种promot格式

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206210846963.png)

## 第三方Media插入

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206210949349.png)

其中`platform` 是平台名称的小写，`ID` 是音视频ID,目前支持的平台如下

用以下语法嵌入社交媒体平台的视频/音频，语法与效果如下图

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206211027840.png)

## 脚注与反向脚注

**正向脚注**

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206211110969.png)

**反向脚注**

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206211135850.png)