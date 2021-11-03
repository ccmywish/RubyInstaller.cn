---
layout: post
title:  "发布 RubyInstaller 2.7.2-1, 2.6.6-2 和 2.5.8-2"
author: Lars Kanis，ccmywish
---

RubyInstaller 版本 2.7.2-1, 2.6.6-2 和 2.5.8-2 发布了!这些是维护版本(主要修复bug以及安全问题)

这个版本解决了一些 [最近的issues](https://github.com/oneclick/rubyinstaller2/issues/184) 它们主要与MSYS2包安装和MSYS2更新有关。

它添加了RI文档作为可选的安装组件，该组件很好地集成到Ruby-2.7上的`irb`中，并改进了[`ridk use`](https://github.com/oneclick/rubyinstaller2/wiki/The-ridk-tool)命令。

此外，打包的库以及TLS CA列表也有一些更新。

See [ruby-2.7.2 release notes](https://www.ruby-lang.org/en/news/2020/10/02/ruby-2-7-2-released/) as well as the RubyInstaller CHANGELOG files for [RubyInstaller-2.5.8-2](https://github.com/oneclick/rubyinstaller2/blob/master/CHANGELOG-2.5.md#rubyinstaller-258-2---2020-10-06), [RubyInstaller-2.6.6-2](https://github.com/oneclick/rubyinstaller2/blob/master/CHANGELOG-2.6.md#rubyinstaller-266-2---2020-10-06) and [RubyInstaller-2.7.2-1](https://github.com/oneclick/rubyinstaller2/blob/master/CHANGELOG-2.7.md#rubyinstaller-272-1---2020-10-06).


不幸的是当前主要的MSYS2包服务器[https://repo.msys2.org](https://repo.msys2.org)处于宕机中。其他可选的hosts会被`pacman`自动选中，但是这个过程会等待很久。
为了避免这个延迟，你也许你可以将host注释掉(下方的第一个命令)，并查看剩余的hosts(下方的第二个命令)
```
ridk exec sh -c "sed -e '/repo.msys2.org/ s/Serv/#Serv/' -i /etc/pacman.d/mirrorlist.*"
ridk exec sh -c "cat /etc/pacman.d/mirrorlist.*"
```

所有的文件都可以在[下载页面]({{ "/downloads/" | relative_url }})找到!

