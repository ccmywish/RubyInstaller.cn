---
layout: post
title:  "发布 RubyInstaller 3.0.3-1, 2.7.5-1 和 2.6.9-1 released"
author: Lars Kanis, ccmywish
---
RubyInstaller versions 3.0.3-1, 2.7.5-1 和 2.6.9-1 发布了。这些是维护版本，修复了一些缺陷和安全问题。

查看 [ruby-3.0.3 官方发布](https://www.ruby-lang.org/en/news/2021/11/24/ruby-3-0-3-released/), [ruby-2.7.5 官方发布](https://www.ruby-lang.org/en/news/2021/11/24/ruby-2-7-5-released/) 和 [ruby-2.6.9 官方发布](https://www.ruby-lang.org/en/news/2021/11/24/ruby-2-6-9-released/) 以获得详情.

一个之前的RubyInstaller-2.6.x 或 2.7.x安装 <b>不应当</b> 被通过将RubyInstaller-3.0.x安装同一目录下直接更新。这是因为一些带有C语言扩展的gem在ruby-2.7和3.0之间并不兼容。最好像我们提议的，使用新的目录来存放3.0.x

所有安装程序都放在了[下载区域]({{ "/downloads/" | relative_url }})!
