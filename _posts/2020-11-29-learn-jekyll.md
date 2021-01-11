---
layout: post
title: Jekyll 基础学习
date: 2020-11-29 10:03:00 +08000
categories: 前端
tags: jekyll
---

## 目录结构说明

- `_[dirname]` : 表示 `jekyll` 内部约定的目录。
  - \_layouts : 表示包含布局文件。
  - \_includes : 表示存放相关的模板文件。
  - \_posts : 存放文章
  - \_sass : 样式
- \_config.yml : 站点配置文件，可以在模板中通过 `site.var` 读取相关的配置。
- index.md : 博客入口页面。
- about.md : 博客关于页面。

<img src="" width="303" height="392">

  {%raw%}
  表达式: `{{express}}`
  语句：`{% statement %}`
{%endraw%}

Example:

{% highlight js linenos %}
const DEVELOPER_SIGN_KEY = 'developer_sign_key';
async function getSignPrivilege(orgInfo: orgInfoModel, isDeveloper: boolean) {
  const orgId = orgInfo.id;
  const orgPrivileges = (store.state.orgPrivileges || {}) as { [key: string]: any };
  const editKey = isDeveloper ? 'org.edit' : 'agent.edit';

  let result: { [key: string]: any } = {};

  if (has(orgPrivileges, '${orgId}.${contractPrivilegeKey}')) {
    result = orgPrivileges;
  } else {
    result = await getOrgPrivileges([
      [editKey, { orgId }],
      [DEVELOPER_SIGN_KEY, { orgId }],
    ]);
  }

  return result[orgId] ? { ...result[orgId] } : {};
}
{% endhighlight %}
