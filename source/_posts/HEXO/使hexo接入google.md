---
layout: post
title: HEXO操作指南（三）
description: 将HEXO接入Google搜索中
date: 2019-11-17 14:09:10
comments: true
categories: Technology
tags: HEXO
toc: true
---
如果你不主动提交你的博客地址给各大搜索引擎，那么即使你站内优化做得再好，搜索引擎根本都不知道你的博客的存在。 为了让Google收录我的博客，就得向[Google站长工具](https://www.google.com/webmasters)提交我们得Sitemap。
## Google验证
Google有多种验证方法，这里我选用Html标记，在`layout/_partial/head.pug`文件内输入`<meta name="google-site-verification" content="xxxxxxxxxxxxxxxxxx" />`。
接着
```python
hexo c
hexo d
```
上传完毕点击验证便可验证成功。

## Sitemap调用
首先安装sitemap插件：
```python
npm install hexo-generator-sitemap --save
```
接着在`_config.yml`文件后添加：
```python
Plugins:
  - hexo-generator-sitemap

sitemap:
  path: sitemap.xml

```
**重点**，把`_config.yml`中的`url`改成自己的域名，否者最终提交后会出现**站点地图可读取，但存在错误**。这样的字眼。
```python
url: https://huixueee.com
```
这时`public`文件夹内会出现相应的sitemap文件，随后：
```python
hexo c
hexo d
```
在Google search console中选择站点地图->添加/测试站点地图，提交后便大功告成。