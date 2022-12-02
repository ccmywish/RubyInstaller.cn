---
layout: post
title:  "发布 RubyInstaller 3.1.0-1"
authors: 
  - Lars Kanis
  - ccmywish
---
RubyInstaller-3.1.0-1 发布了! 此版本提供了一系列新功能与新改进。请查看[Ruby-3.1.0官方发布通告](https://www.ruby-lang.org/en/news/2021/12/25/ruby-3-1-0-released/)获取详情。

RubyInstaller-3.1.0-x64更换了一个C-runtime，即使用`UCRT`来替换旧的`MSVCRT`.

这个现代C运行时环境带来了与C标准以及与使用Visual Studio编译的库之间更好的兼容性。

查看功能请求[这里](https://bugs.ruby-lang.org/issues/17845)。
这里有[几个平台的字符串问题](https://github.com/ruby/ruby/pull/4599)随着本次新发布而改变。

尤其是，现在的Ruby和Gem的Platform已经从`x64-mingw32`更换为`x64-mingw-ucrt`, 并且MSYS2包前缀现在也变为`mingw-w64-ucrt-x86_64-`

RubyInstaller的Devkit现在打包了基于`UCRT`的MINGW包。 

`ridk install`可以被用于安装这些包到MSYS2一个之前的或共享的位置。

这里有一些随之而来而问题，比如无缝地[与Github Actions集成](https://github.com/ruby/setup-ruby/issues/193)和与UCRT相关的[跨平台编译](https://github.com/rake-compiler/rake-compiler-dock/issues/61)。

请注意，一些Gems现在仍然与Windows上的Ruby-3.1不兼容。
这种情况下，你应当停留在3.0, 直到3.1被很好的支持。

一个之前的RubyInstaller-3.0.x或2.7.x安装<b>不应当</b>被通过将RubyInstaller-3.0.x安装同一目录下直接更新。这是因为一些带有C语言扩展的gem在ruby-3.0和3.1之间并不兼容。最好像我们提议的，使用新的目录来存放3.1.x

所有安装程序都放在了[下载区域]({{ "/downloads/" | relative_url }})!
