# CONTRIBUTING

若您有新的想法，或发现了存在的问题，或可改善的地方(比如更好的UI)，或者若您想要参与开发与日常维护，请您在[issues](https://gitee.com/RubyKids/rubyinstaller.cn/issues) 处反馈，并请阅读下面的内容。我将非常乐意接受任何对此项目的贡献与努力。

<br>

## TODO

1. 导航栏点击后应显示我们当前所在位置
2. 添加RSS feed

<br>

## 文件

1. `news/_posts` 目录存放文章`
2. `_data` 目录存放下载链接
3. `_about` 目录存放关于页面
4.  `downloads.md` 下载页面右边侧边栏的信息
5. `_config.yml` Jekyll配置文件
6. `_site` Jekyll生成的目录

<br>

## 命令行

```bash
# 安装依赖
bundle

# 在Gemfile的指定下更新依赖，更新Gemfile.lock
bundle update

# 查看jekyll版本
jekyll -v

# 在 _site 目录下生成
bundle exec jekyll build    
```

<br>

## 维护内容和要点

1. 编辑文章时中英文之间不需要有空格，因为其CSS的设置使得无空格时更加清晰。
2. 下载链接请参考以往的上海交通大学镜像地址，它和Github的下载地址略有不同，多了一个目录
3. 下载链接加粗需要使用 `recommended: true`，请和上游保持一致

<br>
