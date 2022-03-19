# 网站维护

1. `_posts` 目录存放文章
2. `_data` 目录存放下载链接
3. `_config.yml` Jekyll配置文件
4. `_site` 生成的目录
5. `downloads.md` 下载页面右边侧边栏的信息

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

## 维护内容

1. 编辑文章时中英文之间不需要有空格，因为其CSS的设置使得无空格时更加清晰。
2. 下载链接请参考以往的上海交通大学镜像地址，它和Github的下载地址略有不同，多了一个目录
3. 下载链接加粗需要使用 `recommended: true`，请和上游保持一致


