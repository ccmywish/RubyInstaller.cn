---
layout: post
title:  "发布 RubyInstaller 3.1.2-1, 3.0.4-1, 2.7.6-1 和 2.6.10-1"
authors:
  - Lars Kanis
  - ccmywish
---
RubyInstaller 3.1.2-1, 3.0.4-1, 2.7.6-1和2.6.10-1发布了。这些是维护版本，修复了一些缺陷和安全问题。请分别查看[Ruby 3.1.2发布说明](https://www.ruby-lang.org/en/news/2022/04/12/ruby-3-1-2-released/), [Ruby 3.0.4发布说明](https://www.ruby-lang.org/en/news/2022/04/12/ruby-3-0-4-released/), [Ruby 2.7.6发布说明](https://www.ruby-lang.org/en/news/2022/04/12/ruby-2-7-6-released/) 和 [Ruby 2.6.10发布说明](www.ruby-lang.org/en/news/2022/04/12/ruby-2-6-10-released/)获得详情.

一个之前的RubyInstaller 2.7.x或3.0.x安装<b>不应当</b>被通过将RubyInstaller 3.1.x安装同一目录下直接更新。这是因为一些带有C语言扩展的Gem在Ruby 3.0和3.1之间并不兼容。最好像我们提议的，使用新的目录来存放3.1.x

所有安装程序都放在了[下载区域]({{ "/downloads/" | relative_url }})!
