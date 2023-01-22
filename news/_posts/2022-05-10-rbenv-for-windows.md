---
layout: post
title:  "推荐您使用rbenv for Windows在命令行上安装管理多个Ruby版本"
author: ccmywish
---

无论您是初级用户还是高级用户，我都建议您直接使用`rbenv for Windows`，从命令行上安装管理多个Ruby版本，从而无需手动处理您不熟悉的内容(比如`MSYS2`,`ridk`工具等)。我们已经利用了该站所提供的下载链接，所以您可放心使用，不会遇到网络问题。

<br>

## 安装

在终端中运行:

<!-- 注意，使用Markdown语法 ``` 是无效的 -->
{% highlight PowerShell %}
mkdir "C:\Ruby-on-Windows"
git -C "C:\Ruby-on-Windows" clone "https://github.com/ccmywish/rbenv-for-windows" rbenv
{% endhighlight %}

然后在`$profile`中添加这些内容:

{% highlight PowerShell %}
# rbenv for Windows
$env:RBENV_ROOT = "C:\Ruby-on-Windows"

# 国内用户使用内置镜像
# 注意，这一行必须放在init之前
$env:RBENV_USE_MIRROR = "CN"

& "$env:RBENV_ROOT\rbenv\bin\rbenv.ps1" init
{% endhighlight %}

<br>

## 链接参考

1. [Ruby China上的介绍帖](https://ruby-china.org/topics/42378)
2. [位于Github上的源代码](https://github.com/ccmywish/rbenv-for-windows)
3. [位于Gitee上的源代码](https://gitee.com/ccmywish/rbenv-for-windows)

下载安装方式均在上述链接中展示。
