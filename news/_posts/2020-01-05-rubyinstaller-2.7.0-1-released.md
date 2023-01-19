---
layout: post
title:  "发布 RubyInstaller 2.7.0-1"
authors:
  - Lars Kanis
  - ccmywish
---
RubyInstaller 2.7.0-1发布了！查看[Ruby 2.7.0发布说明](https://www.ruby-lang.org/en/news/2019/12/25/ruby-2-7-0-released/)和[RubyInstaller CHANGELOG](https://github.com/oneclick/rubyinstaller2/blob/master/CHANGELOG-2.7.md)来获取详情。

请注意，一些Gems还不兼容Windows上的Ruby 2.7。因此，您应该继续使用2.6，直到2.7得到良好的支持为止，除非您想做出贡献并修复剩余的问题。

到目前为止，RubyInstaller使用[rb-readline](https://github.com/ConnorAtherton/rb-readline)作为`irb`和其他交互式控制台应用程序的行编辑器。这是因为GNU readline库在Windows上不能正常工作。

然而`rb-readline`基本上没有被维护了，并且有很多bug。幸运的是，Ruby 2.7引入了[Reline](https://github.com/ruby/reline)作为一个Readline的纯Ruby实现。它在Windows上工作的很好，所以RubyInstaller 2.7.0-1使用`Reline`替换以前的`rb-readline`.

另一个变化是RubyInstaller 2.7.0-1默认使用UTF-8作为外部字符编码。Ruby源代码，MSYS2工具和PowerShell core已经默认使用UTF-8了。这个变化同时修复了一些Reline的问题，并增加了与其他操作系统的兼容性。

UTF-8编码将在环境变量`RUBYOPT`被设置为`-Eutf-8`时开启，因此这影响所有安装在本系统上的Ruby版本。要还原至传统的的依赖于国家的codepage为外部编码，请到Windows系统设置中，从用户和系统环境变量中删除`RUBYOPT`.

如果在Ruby 2.7上工作良好，`Reline`以及默认UTF-8这两个功能都将被向后移植到下一个RubyInstaller 2.4, 2.5和2.6系列的版本,所以请使用[issue tracker](https://github.com/oneclick/rubyinstaller2/issues) 来给予我们正面或负面的反馈!

所有的安装程序都可以在[下载页面]({{ "/downloads/" | relative_url }})找到!
All binaries are available in the [Download section]({{ "/downloads/" | relative_url }})!
