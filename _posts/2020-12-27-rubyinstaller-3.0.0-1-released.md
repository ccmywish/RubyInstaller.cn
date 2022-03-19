---
layout: post
title:  "发布 RubyInstaller 3.0.0-1"
author: Lars Kanis, ccmywish
---
RubyInstaller-3.0.0-1发布了!
新版本伴随了大量的新功能以及改善。查看[Ruby-3.0.0官方发布通告](https://www.ruby-lang.org/en/news/2020/12/25/ruby-3-0-0-released/)获取更多信息。

Ruby-3.0.0完成了在Windows上将UTF-8作为主要字符编码的转变。这个功能为文件系统和环境变量启用了完整的Unicode字符集，并增加了与其他工具和操作系统的兼容性。

请注意，有一些Gems在Windows上还未能与Ruby-3.0完全兼容，这种情况下你也许依然要使用Ruby 2.7，直到3.0版本被完全支持。

<b>不能</b>直接使用RubyInstaller-3.0.x将目标目录放在之前存在的RubyInstaller-2.6.x或2.7.x安装目录下来完成更新。因为伴随有C扩展的Gem在Ruby-2.7和3.0中不兼容。最好使用一个新目录来安装3.0.x 

所有的安装程序都可以在[下载页面]({{ "/downloads/" | relative_url }})找到!
