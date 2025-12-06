---
title: Jekyll博客搭建(六) | 远程仓库推送
author: 0x_716
date: 2025-08-09 22:40:00 +0800
categories: [blog]
tags: [blog]
pin: true
math: true
mermaid: true
image:
  path: assets/cover/blog-6.png
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
---



## 配置Git

```
git config --global user.name "Your Name"
git config --global user.email "youremail@example.com"
```

将“ `Your Name` ”和“ `youremail@example.com` ”替换即可

## 生产SSH密钥对

本地生成SSH密钥对，用于后续与Github进行身份验证

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

- 按Enter键接受SSH密钥对文件默认存储位置
- 在密码提示的时候按两次Enter键

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206212516676.png)

## 启动ssh-agent并添加SSH密钥

```
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa   #这里的SSH密钥位置需要按照自己的来填写
```

##  显示并复制SSH公钥

```
cat ~/.ssh/id_rsa.pub
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206212622205.png)

## 将SSH公钥添加到Github

`GitHub` → `Settings` → `SSH & GPG Keys` → `New SSH key` → `Paste Key`

## 验证与Github的SSH连接

以下两个命令测试连接性

```
ssh -T git@github.com
ssh -T -p 443 git@ssh.github.com
```

- 应该会看到一条确认身份验证成功的消息

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206212651947.png)

## 推送到远程仓库

```
git add .           # 添加所有更改到暂存区
git commit -m "第一篇blog"  # 提交暂存区的更改到本地仓库
git push origin main 推送到远程仓库分支
```

提交推送到 GitHub 仓库后，会自动触发 GitHub Actions 工作流程

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251206212718189.png)