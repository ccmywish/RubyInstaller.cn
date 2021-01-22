---
layout: downloads
title: 下载
permalink: /downloads/
---

### 我应该下载哪个版本？

如果您不知道要安装什么版本，并且正在开始使用Ruby，我们建议您使用<b>Ruby+Devkit 2.7.X（x64）</b>安装程序。它提供了最多的兼容gems，并将msys2devkit与Ruby一起安装，因此可以立即编译带有C扩展的gems。仅当必须使用自定义32位本机DLL或COM对象时，才建议使用32位(x86)版本。

<br>

### 如何更新？

通过运行新的安装程序版本，Ruby可以更新到最新的补丁版本(例如从2.6.1到2.6.4)，已安装的gem不会被覆盖，并且将在不重新安装的情况下与新版本一起工作。对于这些更新安装，使用RubyInstaller而不使用Devkit就足够了。Devkit可以使用“ridk install”命令单独更新。

如果新的Ruby版本来自不同的稳定分支，那么请使用新的目标目录进行安装。也就是说，以前的RubyInstaller-2.6.x安装<b>不应该通过将RubyInstaller-2.7.x安装到同一目录中来更新。这是因为带有C扩展的gems在ruby-2.6和2.7之间不兼容。

<br>

### RubyInstaller-head

RubyInstaller head是[Ruby开发分支](https://github.com/ruby/ruby/)的每日更新版本。它可以用于gems或应用程序上的持续集成测试（CI），因此您可以为Ruby核心即将发生的变化做好准备。

在[Github发行版部分](https://github.com/oneclick/rubyinstaller2/releases/tag/rubyinstaller-head)中提供了下载链接。

<br>

### 有开发工具包吗？

RubyInstaller使用[MSYS2工具链](http://www.msys2.org)作为它的开发工具。它作为可选组件捆绑到<b>Ruby+Devkit</b>安装程序版本中，因此不需要额外的下载/安装。

MyS2是为了构建Ruby的本地C/C++扩展而需要的，并且对于[Ruby on Rails](https://rubyonrails.org)来说是必需的。

此外，它还允许下载和使用Ruby经常依赖的[数百个开源库](https://github.com/Alexpux/MINGW-packages)。MSYS2开发环境可以通过“ridk enable”在运行的“cmd”或powershell控制台中激活。这会在搜索路径中添加诸如make、gcc、pacman或sh之类的命令。在[Wiki](https://github.com/oneclick/rubyinstaller2/wiki/The-ridk-tool)中查看更多信息。

RubyInstaller是在发布之日用最新的GCC编译的。