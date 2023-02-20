---
translated:
  on: 2023-02-20
  by: ccmywish
  original_link: https://github.com/oneclick/rubyinstaller2/blob/RubyInstaller-3.2.1-1/CHANGELOG-3.2.md#rubyinstaller-321-1---2023-02-09
---

## RubyInstaller 3.2.1-1 [2023-02-09]

### 变化
- 更新至 Ruby 3.2.1, 查看[官方发行说明](https://www.ruby-lang.org/en/news/2023/02/08/ruby-3-2-1-released/)。
- 更新SSL CA证书列表，并更新至 OpenSSL-3.0.8.
- 将OpenSSL目录从`<install-path>/ssl/`移动至`<install-path>/etc/ssl/`来追随上游的变化: https://github.com/msys2/MINGW-packages/commit/2f97826e8a8fce0b9a49da7ea2bffbab7ce98eb5
- 允许home目录带有空格（在安装gems到用户home时）#332
- 不要覆盖 `GEM_HOME` 或 `BUNDLE_SYSTEM_BINDIR` 如果已经存在的话
- 不要将bindir设置为不存在的目录
  这个和 https://github.com/rubygems/rubygems/issues/6332 相关


## RubyInstaller 3.2.0-1 [2022-12-29]

这是基于Ruby 3.2.0的第一个版本: https://www.ruby-lang.org/en/news/2022/12/25/ruby-3-2-0-released/

### 与 RubyInstaller 3.1.3-1 相比的变化
- 添加安装程序新的对话框来让用户选择 `per-user(单个用户)` 还是 `all-users(全部用户)` 安装模式。
  查看[Wiki中的安装模式描述](https://github.com/oneclick/rubyinstaller2/wiki/FAQ#user-content-install-mode)来获取更多信息。
- 添加安装程序命令选项 `/ALLUSERS` 和 `/CURRENTUSER` 来静默安装
  对于静默安装，请查看: https://github.com/oneclick/rubyinstaller2/wiki/FAQ#user-content-silent-install
- 如果用户在一台`机器全局安装的Ruby`下没有写权限，则自动将gem安装到用户的私有home目录
- 使用`ridk use`列出不仅是用户自己安装的rubies，并且包括整个机器范围内的rubies
- 为安装目录添加完全管理员访问权限。
  如果没有这个权限，管理员必须使用`takeown`命令重新获得对用户安装目录（per-user installation）的写访问权。
- 对MSYS /tmp 目录设置适当的权限，使每个用户都可以创建和使用文件，而不能读取和修改其他用户的文件。
  这是整机安装模式（machine-wide）下所需要的。
- 每次加载rubygems时检查或添加一个系统范围的`gemrc`文件，以防止被其他用户劫持。
- 避免在`TMP`环境变量中使用UNICODE字符来变通解决`gcc`的问题。# 320
- 切换到OpenSSL-3。这对Ruby API有几个影响，并禁用了对遗留加密算法的支持。
  查看 https://github.com/ruby/openssl/blob/master/History.md#version-300 以及 https://github.com/openssl/openssl/blob/master/doc/man7/migration_guide.pod#openssl-30
