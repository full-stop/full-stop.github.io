---
layout: post
title: Jekyll 基础学习
date: 2020-11-29 10:03:00 +08000
categories: jekyll
---


## 目录结构说明

* `_[dirname]` : 表示 `jekyll` 内部约定的目录。
    * _layouts : 表示包含布局文件。
    * _includes : 表示存放相关的模板文件。
    * _posts : 存放文章
    * _sass : 样式
* _config.yml : 站点配置文件，可以在模板中通过 `site.var` 读取相关的配置。
* index.md : 博客入口页面。
* about.md : 博客关于页面。 
{%raw%}
表达式: `{{express}}`
语句：`{% statement %}` 

Example:

```javascript
{% if page.title %} {{page.title | escape}}
{% else %} {{site.title | escape}}
{% endif %}
```

{%endraw%}