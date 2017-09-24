---
title: 常用Markdown语法备忘
date: 2017-05-15 13:30:35
tags: markdown
categories: markdown
---

### 公式

行间

$$a = b^2$$

行内公式\\(a = b^2\\)

### 代码

```c++
#include<stdio.h>
int main(int, char**)
{
    return 0
}
```
<!-- more -->

### 文本居中引用

{% cq %}
人的一切痛苦，本质上都是对自己无能的愤怒。

**王小波**
{% endcq %}

### 标注
{% note default %} Content (md partial supported) {% endnote %}
{% note primary %} Content (md partial supported) {% endnote %}
{% note success %} Content (md partial supported) {% endnote %}
{% note info %} Content (md partial supported) {% endnote %}
{% note warning %} Content (md partial supported) {% endnote %}
{% note danger %} Content (md partial supported) {% endnote %}

### 手动分割显示更多
```
<!-- more -->
```

### 链接
```
[Hexo](https://hexo.io/)
```
[Hexo](https://hexo.io/)

### 插入图片
```
![头像](/images/avatar_tcye.jpg)
```
![头像](/images/avatar_tcye.jpg)