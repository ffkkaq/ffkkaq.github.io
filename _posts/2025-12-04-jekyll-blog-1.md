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


## 基础环境与技术栈

- **Ubuntu 24.04.3**
- **Jekyll** ：基于 Ruby 的静态站点生成器
- **Chirpy Theme**：响应式 Jekyll 主题
- **GitHub Pages**：免费静态托管Jekyll网站

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251205171226732.png)

## Jekyll、Git、依赖安装

> 经测试,`Ubuntu24.04.03`包管理器安装的Ruby最新版只能到3.0.x，而Chirpy则需要Ruby版本大于3.1.x，所以这里使用`rbenv`版本管理器进行安装Ruby

- 更新包列表
- 安装Git、依赖

```
sudo apt update
sudo apt install -y git curl libssl-dev libreadline-dev zlib1g-dev autoconf bison build-essential libyaml-dev libncurses5-dev libffi-dev libgdbm-dev zlib1g-dev
```

- 使用 `curl` 安装 `rbenv`版本管理器
- 将rbenv添加到shell配置文件中
- 检查 `rbenv` 是否正常工作

```
curl -fsSL https://github.com/rbenv/rbenv-installer/raw/main/bin/rbenv-installer | bash
echo 'export PATH="$HOME/.rbenv/bin:$PATH"' >> ~/.bashrc 
echo 'eval "$(rbenv init -)"' >> ~/.bashrc 
source ~/.bashrc
rbenv -v
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251205171324853.png)

Jekyll要求Ruby版本必须大于`2.7.0`，且Chirpy主题则需要Ruby版本大于3.1.x，这里选择安装`3.2.3`

```
rbenv install 3.2.3
rbenv global 3.2.3
ruby -v
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251205171502740.png)

## 配置Ruby Gems环境

为RubyGems设置专用目录，简化 Gem 管理：

```
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251205171621243.png)

## 安装Jekyll和Bundler

RubyGems 环境配置完成，继续安装 Jekyll 和 Bundler，安装后通过检查版本来确保Jekyll已正确安装，此时安装的版本为 4.4.1，本地Jekyll Chirpy环境已经配置完成

```
gem install jekyll bundler
jekyll -v
```

![](https://raw.githubusercontent.com/ffkkaq/imageHost/main/img/20251205171727220.png)





