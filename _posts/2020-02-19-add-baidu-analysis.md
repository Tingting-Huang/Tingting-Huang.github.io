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

**为你的32位ID，

### 3 在_includes/head.html加入上图中所有代码，完成统计功能

### 4 在_layouts/default.html中添加

``` <script async src="//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js"></script>
```

在_includes目录下的footer.html中添加如下代码，这样文章底部有了统计访问量功能

```<span id="busuanzi_container_site_pv">本站总访问量：<span id="busuanzi_value_site_pv"></span>次</span>```

在_layouts目录下的post.html中添加如下代码，这样每篇文章有了统计访问量功能

```<span id="busuanzi_container_page_pv"> | 访问量：<span id="busuanzi_value_page_pv"></span> 次</span>```

