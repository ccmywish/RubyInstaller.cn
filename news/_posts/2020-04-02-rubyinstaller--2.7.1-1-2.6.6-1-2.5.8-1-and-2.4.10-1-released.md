---
layout: post
title:  "发布 RubyInstaller 2.7.1-1, 2.6.6-1, 2.5.8-1 和 2.4.10-1"
authors:
  - Lars Kanis
  - ccmywish
---

RubyInstaller 2.7.1-1, 2.6.6-1，2.5.8-1和2.4.10-1发布了! 这些是维护版本(主要修复Bug以及安全问题)。

查看[Ruby 2.4.10发布说明](https://www.ruby-lang.org/en/news/2020/03/31/ruby-2-4-10-released/), [Ruby 2.5.8发布说明](https://www.ruby-lang.org/en/news/2020/03/31/ruby-2-5-8-released/), [Ruby 2.6.6发布说明](https://www.ruby-lang.org/en/news/2020/03/31/ruby-2-6-6-released/) 和 [Ruby 2.7.1发布说明](https://www.ruby-lang.org/en/news/2020/03/31/ruby-2-7-1-released/) 以及 RubyInstaller CHANGELOG 文件: [RubyInstaller 2.4.10-1](https://github.com/oneclick/rubyinstaller2/blob/master/CHANGELOG-2.4.md#rubyinstaller-2410-1---2020-04-02), [RubyInstaller 2.5.8-1](https://github.com/oneclick/rubyinstaller2/blob/master/CHANGELOG-2.5.md#rubyinstaller-258-1---2020-04-02), [RubyInstaller 2.6.6-1](https://github.com/oneclick/rubyinstaller2/blob/master/CHANGELOG-2.6.md#rubyinstaller-266-1---2020-04-02) 和 [RubyInstaller 2.7.1-1](https://github.com/oneclick/rubyinstaller2/blob/master/CHANGELOG-2.7.md#rubyinstaller-271-1---2020-04-02).
打包的 OpenSSL版本现更新至 1.0.2u (Ruby-2.4.x) 以及 1.1.1f (Ruby-2.5+).

所有以上RubyInstaller版本均切换使用 [Reline](https://github.com/ruby/reline)作为`irb`以及其他交互式控制台程序的行编辑器(line-editor)。同时，所有的RubyInstaller现在默认使用UTF-8来作为外部的字符编码。这两个我们已经[在RubyInstaller-2.7.1-1中介绍过的变化]({% post_url 2020-01-05-rubyinstaller-2.7.0-1-released %}) 现在已经向后移植到 RubyInstaller 2.4, 2.5 and 2.6中。

请注意，RubyInstaller 2.4.10-1 将会是Ruby 2.4系列的最后版本，这是因为Ruby 2.4和OpenSSL 1.0.x的支持都结束了。

所有的安装程序都可以在[下载页面]({{ "/downloads/" | relative_url }})找到!
