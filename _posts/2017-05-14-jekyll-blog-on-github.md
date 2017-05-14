---
layout: post
title: "使用jekyll在github pages 上写博客"
date: 2017-05-14 23:27:20 +0800
categories: 教程
tags: 博客, jekyll, github pages
---
jekyll 允许你用Markdown语法来写博客， 然后很轻松的发布到github pages 上去， 这是完全免费的。

这篇教程将教会你如何利用jekyll和github pages, 在Ubuntu环境下轻松的构建一个静态博客网站。

首先安装jekyll
{% highlight bash %}

apt install jekyll

{% endhighlight %}

然后创建你的工程目录, 创建一个叫myblog的工程

{% highlight bash %}

jekyll new myblog

{% endhighlight %}

然后你的myblog的目录结构会像下面这样