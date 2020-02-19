---
layout: post
title:  "jekyll添加百度统计"
subtitle:   ""
date:   2020-02-19 21:02:54
categories: github 
tags: baidutongji
---

* content
{:toc}


### 1 登录百度账号，获取百度统计代码;
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/1百度统计.jpg)

### 2 修改_config.yml;

加入```baidu-analysis: ********************************```

**为你的32位ID，

### 3 在_includes/head.html加入图1代码，完成统计功能.

### 4 添加文章访问量功能.

* 在_includes/head.html中添加以下代码;

``` <script async src="//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js"></script>
```

* 在_includes/footer.html中添加以下代码，文章底部有了统计访问量功能;

```本站总访问量<span id="busuanzi_value_site_pv"></span>次，本站访客数<span id="busuanzi_value_site_uv"></span>人次，本文总阅读量<span id="busuanzi_value_page_pv"></span>次```

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/底部访问量.jpg)

* 在_layouts/post.html中添加以下代码，每篇文章有了统计访问量功能.

```<span id="busuanzi_container_page_pv"> | 访问量：<span id="busuanzi_value_page_pv"></span> 次</span>```

