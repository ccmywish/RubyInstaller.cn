不确定要下载哪个版本？请阅读右栏中的建议。

本站暂时仅提供64位devkit镜像，这也是大多数人需要的版本。

###  包含 Devkit

<ul>
  {% assign dls = site.data.downloads | where: "filetype", "ridkexe" | where: "show", "true" %}
  {% include downloadlinks.html dls=dls %}
</ul>

