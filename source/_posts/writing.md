---
title: writing
date: 2023-10-15 19:36:26
tags:
index_img: /img/default.jpg
banner_img: /img/default.jpg
hide: true
---

参考自[配置文档](https://hexo.fluid-dev.com/docs/guide)

### Fluid 主题文章页配置

```yaml
---
title: 文章标题
date:
tags: [Hexo, Fluid]
excerpt: 文章摘要
sticky: 文章排序，数值越大文章越靠前
hide: 隐藏文章
index_img: 文章在首页的封面图 # /img/example.jpg
banner_img: 文章页顶部大图 # /img/post_banner.jpg
---
```

### Tag 插件

#### 便签

```md
{% note success %}
文字 或者 `markdown` 均可
{% endnote %}
```

{% note primary %}
primary
{% endnote %}
{% note secondary %}
secondary
{% endnote %}
{% note success %}
success
{% endnote %}
{% note danger %}
danger
{% endnote %}
{% note warning %}
warning
{% endnote %}
{% note info %}
info
{% endnote %}
{% note light %}
light
{% endnote %}

#### 行内标签

```md
{% label primary @text %}
```

可选 Label：
{% label primary @primary %}
{% label default @default %}
{% label info @info %}
{% label success @success %}
{% label warning @warning %}
{% label danger @danger %}

#### 勾选框

```md
{% cb text, checked?, incline? %}
```

#### 按钮

```md
{% btn url, text, title %}
```

{% btn /, text, title %}

#### 组图

```md
{% gi total n1-n2-... %}
![](url)
![](url)
![](url)
![](url)
![](url)
{% endgi %}
```

total：图片总数量，对应中间包含的图片 url 数量
n1-n2-...：每行的图片数量，可以省略，默认单行最多 3 张图，求和必须相等于 total，否则按默认样式
