---
title: "开博第一篇"
description: "Hugo搭建Github Pages博客"
date: "2015-10-11T08:24:28+08:00"
categories: 
    - "随笔"
keywords:
    - "Hugo"
---

在家养病，没事在github上开个博客，以后有想法会在这更新。

工具使用的是[Hugo](https://gohugo.io)，一个小巧、快速的静态页面生成引擎，参考了这篇教程[Hosting on GitHub Pages](https://gohugo.io/tutorials/github-pages-blog/)。

步骤如下：

1. 1. 下载[Hugo][]并安装，然后将hugo加入系统PATH中。（可参考[Installing Hugo][]）
2. 2. 在Github中创建一个 `<your-project>-hugo` 的repository ，用于保存Hugo的内容。
3. 3. 在Github中创建一个 `<username>.github.io` 的repository ，用于保存Hugo中的public目录，也就是博客的静态内容。
4. 4. `git clone <<your-project>-hugo-url> && cd <your-project>-hugo`
5. 5. 本地调试：`hugo server --watch`
6. 6. 调试无误后，ctrl+c结束调试。`rm -rf public`
7. 7. `git submodule add git@github.com:<username>/<username>.github.io.git public`。如果不是第一次提交，则使用`git submodule update --init --recursive`。
8. 8. 执行`deploy.sh "Your optional commit message"`

稍等片刻，就可以在<http://username.github.io/>看到你的博客了。

最后，也不要忘记了提交hugo博客的修改。


[Hugo]: https://github.com/spf13/hugo/releases/latest
[Installing Hugo]: https://gohugo.io/overview/installing/