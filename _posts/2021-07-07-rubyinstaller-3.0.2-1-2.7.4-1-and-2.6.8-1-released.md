---
layout: post
title:  "发布 RubyInstaller 3.0.2-1, 2.7.4-1 和 2.6.8-1"
author: Shaun Mabbs，ccmywish
---

RubyInstaller versions 3.0.2-1, 2.7.4-1 and 2.6.8-1 已经发布了。这些是维护版本，修复了一些缺陷和安全问题。

开启了对超过260个字符的路径长度的支持。查阅 [829ab9d](https://github.com/oneclick/rubyinstaller2/commit/829ab9d9798d180655b6b336797b1087bfa82f5c)

增加了 `racc`, `rbs`, `typerof` 可知性文件到 /bin 目录。查阅 [#231](https://github.com/oneclick/rubyinstaller2/issues/231)


查看 [ruby-3.0.2 官方发布](https://www.ruby-lang.org/en/news/2021/07/07/ruby-3-0-2-released/), [ruby-2.7.4 官方发布](https://www.ruby-lang.org/en/news/2021/07/07/ruby-2-7-4-released/) 和 [ruby-2.6.8 官方发布](https://www.ruby-lang.org/en/news/2021/07/07/ruby-2-6-8-released/) 以获得详情。

请注意，一些gem在Windows上与Ruby-3.0并不兼容，这种情况下，你可能需要依然使用2.7直到3.0被很好的支持。

一个之前的RubyInstaller-2.6.x 或 2.7.x安装 <b>不应当</b> 被通过将RubyInstaller-3.0.x安装同一目录下直接更新。这是因为一些带有C语言扩展的gem在ruby-2.7和3.0之间并不兼容。最好像我们提议的，使用新的目录来存放3.0.x

所有安装程序都放在了[下载区域]({{ "/downloads/" | relative_url }})!