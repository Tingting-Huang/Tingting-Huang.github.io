---
layout: post
title:  "jekyll添加百度统计"
subtitle:   ""
date:   2020-02-19 20:02:54
categories: github 
tags: baidutongji
---

* content
{:toc}


### 1 登录百度账号，获取百度统计代码

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/fork.jpg)


### 2 修改_config.yml

加入```baidu-analysis: ********************************```

### 3 在_includes中新建文件baidu-anaylysis.html加入以下代码
```
<script>
  var _hmt = _hmt || [];
  (function() {
    var hm = document.createElement("script");
	**hm.src = "https://hm.baidu.com/hm.js?<%= theme.baidu_analytics %>";**
    var s = document.getElementsByTagName("script")[0];
    s.parentNode.insertBefore(hm, s);
  })();
</script>
```
注意：与其他博文相比，```hm.src = "https://hm.baidu.com/hm.js?<%= theme.baidu_analytics %>";```此处加了https，百度统计就会检测代码安装正确。

### 4 在_layouts/default.html中添加

``` {% include baidu-analysis.html %}```