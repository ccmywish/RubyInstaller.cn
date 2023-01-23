---
layout: post
title:  "发布 RubyInstaller 3.0.2-1, 2.7.4-1 和 2.6.8-1"
authors:
  - Shaun Mabbs
  - Lars Kanis
  - ccmywish
---

RubyInstaller 3.0.2-1, 2.7.4-1和2.6.8-1发布了。这些是维护版本，修复了一些缺陷和安全问题。

开启了对超过260个字符的路径长度的支持。查阅[829ab9d](https://github.com/oneclick/rubyinstaller2/commit/829ab9d9798d180655b6b336797b1087bfa82f5c)

增加了`racc`, `rbs`, `typeprof`可执行文件到`/bin`目录。查阅 [#231](https://github.com/oneclick/rubyinstaller2/issues/231)


查看[Ruby 3.0.2发布说明](https://www.ruby-lang.org/en/news/2021/07/07/ruby-3-0-2-released/), [Ruby 2.7.4发布说明](https://www.ruby-lang.org/en/news/2021/07/07/ruby-2-7-4-released/)和[Ruby 2.6.8发布说明](https://www.ruby-lang.org/en/news/2021/07/07/ruby-2-6-8-released/)获悉详情。

请注意，一些Gem在Windows上与Ruby 3.0并不兼容，这种情况下，你可能需要依然使用2.7直到3.0被很好的支持。

一个之前的RubyInstaller 2.6.x或2.7.x安装<b>不应当</b>被通过将RubyInstaller 3.0.x安装同一目录下直接更新。这是因为一些带有C语言扩展的Gem在Ruby 2.7和3.0之间并不兼容。最好像我们提议的，使用新的目录来存放3.0.x

所有安装程序都放在了[下载区域]({{ "/download/" | relative_url }})!
