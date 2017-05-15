---
layout: post
title: "使用jekyll在github pages 上写博客"
date: 2017-05-14 23:27:20 +0800
categories: 教程
tags: 博客, jekyll, github pages
---
-------------------------------
## 创建我们的第一篇文章
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

![jekyll-dir-tree](http://opyfqi9od.bkt.clouddn.com//blog/jekyll_dir_tree.png)

然后_post目录下开始写第一篇博客吧， 就取名叫my-first-blog吧。

在_post目录下新建一个文件， 文件名必须是年月日再加上文件名， 就像这样

**YYYY-MM-DD-my-first-blog.md**

然后在文件头部加上yaml语法的头部信息, 就像这样

{% highlight yaml %}

    ---
    layout: post
    title: "使用jekyll在github pages 上写博客"
    date: 2017-05-14 23:27:20 +0800
    categories: 教程
    ---

{% endhighlight %}

然后就可以在头部信息下面写你的博客内容了。 

我在博客中写入

> 这是我的第一篇博客， wellcome to my blog.

这样我们的第一篇博客就写好了。

-------------------------
## 上传到github pages

下面我们要做的就是把我们的静态博客网站上传到github pages 的免费个人主页。这是github pages 的官方网站[GitHub Pages](https://pages.github.com/)

本文假定读者对 git 和 github 有初步的了解, 如果不了解也没关系， 只要照着做就好了。 这里有[git的简明指南](http://rogerdudler.github.io/git-guide/index.zh.html)和[github的教程](https://github.com/lavor-zl/Github-Git/blob/master/%E5%88%9D%E5%85%A5Github.md)。

首先登录你的github账号， 新建一个仓库。

![create-new-github-repositories.png](http://opyfqi9od.bkt.clouddn.com/blog/create-new-github-repositories.png)

仓库的名字必须是你的用户名，必须以github.io作为域名。如下图所示， 然后点击创建就好了。

![createanewrespository.png](http://opyfqi9od.bkt.clouddn.com//blog/createanewrespository.png)

然后在你的myblog目录下初始化一个git仓库, 切换到你的jekyll项目根目录。输入命令。

{% highlight shell %}
    git init
{% endhighlight %}

在根目录下创建一个 **.gitignore** 文件， 文件中添加一句。来忽略**_site/**目录。 

{% highlight shell %}
    _site/
{% endhighlight %}

然后执行命令

{% highlight shell %}
    git add .
    git commit -m 'init commit'

    //添加远程仓库
    git remote add origin https://github.com/username/username.github.io.git // username替换为你的用户名
    git push --set-upstream origin master // 输入这条命令后会提示输入用户名和密码。
    git push

{% endhighlight %}

如果这几条命令没问题，你的静态博客网站就上传到github pages 上面了。

等一分钟， 你在浏览器访问， *https://username.github.io* 你就能看到你写的博客了。

就开始创建仓库麻烦一点， 以后就可以直接在_post 目录下创建一个博客， 然后在项目根目录执行。

{% highlight shell %}

    git add .
    git commit -m 'add a new post'

{% endhighlight %}

就可以上传最新的博客上去了， 是不是很方便。

jekyll 还支持更换主题， 支持插件， 和很多自定义功能。 你可以访问[jekyll的官方文档](http://jekyllcn.com/docs/home/)了解更多。

#### 参考资料：

- [jekyll 中文文档](http://jekyllcn.com/docs/home/)
- [git 简明指南](https://rogerdudler.github.io/git-guide/index.zh.html)
- [github pages主页](https://pages.github.com/)

