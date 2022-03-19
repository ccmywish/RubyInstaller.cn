---
layout: downloads
title: 下载
permalink: /downloads/
---

### 我应该下载哪个版本？

如果您即将开始使用Ruby，但是不知道要安装哪个版本，我们建议您使用<b>Ruby+Devkit 3.1.X（x64</b>安装程序。它提供了数量最多的能够兼容的 Gem，并将<b>MSYS2 Devkit<b>与Ruby一起安装，因此可以立即编译带有C语言扩展的Gem. 仅当您有需求必须使用自定义的32位DLL或COM库(二进制对象文件)时，才建议使用32位（x86）版本。

<br>

### 如何更新？

通过运行新版本的安装程序，Ruby可以更新到最新的补丁版本(例如从3.0.0到3.0.3)，已安装的Gem不会被覆盖，并且将在不重新安装的情况下与新版本一起使用。对于这些更新式安装，使用没有Devkit的普通RubyInstaller(左侧没有显式为您提供链接)就足够了。Devkit可以使用`ridk install`命令单独更新。

如果新的Ruby版本和旧的版本处于不同的稳定版本分支，那么请使用一个新的目录进行安装。也就是说，以前的RubyInstaller-3.0.x安装<b>不应</b>通过将RubyInstaller-3.1.x安装进入同一目录来进行更新。这是因为带有C语言扩展的Gems在Ruby-3.0和3.1之间不兼容。在[常见问题FAQ](https://github.com/oneclick/rubyinstaller2/wiki/FAQ#user-content-update-install)中了解更多信息。

<br>

### RubyInstaller-HEAD

RubyInstaller head是[Ruby开发分支](https://github.com/ruby/ruby/)的每日更新版本。它可以用于gems或应用程序上的持续集成测试(CI)，因此您可以为 Ruby Core 即将发生的变化做好准备。在[Github发行版部分](https://github.com/oneclick/rubyinstaller2/releases/tag/rubyinstaller-head)中提供了构建好的下载链接。它们可以很容易地被集成到[Github Actions](https://github.com/oneclick/rubyinstaller2/wiki/For-gem-developers#user-content-github-actions) 或 [Appveyor](https://github.com/oneclick/rubyinstaller2/wiki/For-gem-developers#user-content-appveyor)

<br>

### 是否需要 Devkit？

RubyInstaller使用[MSYS2工具链](http://www.msys2.org)作为它的开发工具。它作为可选组件捆绑到<b>Ruby+Devkit</b>安装程序版本中，因此不需要额外的下载安装。可以在多个版本的Ruby中共享一个Devkit.

MSYS2是为Ruby构建本机C/C++扩展所必需的，并且对于[Ruby on Rails](https://rubyonrails.org)来说是必需的。

此外，它还允许下载和使用Ruby经常依赖的[数百个开源库](https://github.com/Alexpux/MINGW-packages)。MSYS2开发环境可以通过`ridk enable`在运行的cmd或PowerShell控制台中激活。这会在搜索路径中添加诸如make、gcc、pacman或sh之类的命令。在[Wiki](https://github.com/oneclick/rubyinstaller2/wiki/The-ridk-tool)中查看更多信息。

RubyInstaller是在发布之日用最新的GCC编译的。

<br>

### 速度与便捷性

RubyInstaller在发布之日使用最新的GCC进行编译。安装的Ruby是一个本机Windows应用程序，但它结合了MSYS2丰富的UNIX工具集和MINGW库的大型存储库。

阅读更多关于RubyInstaller及其[替代品](https://rubyinstaller.cn/about/comparison)的信息。

<br>

### 文档

Ruby核心和标准库文档是安装的一部分。我们还推荐使用在线文档 [ruby-doc.org](https://ruby-doc.org/).

The Ruby core- and standard library documentation are included as part of the installation. We also recommend the online documentation, or the HTML version downloadable from ruby-doc.org.

<br>

### 用户支持

享受快乐的Ruby编码吧！让我们知道你的想法，或者如果你有任何问题，请在我们友好的 [RubyInstaller Google Group](https://groups.google.com/group/rubyinstaller)联系

