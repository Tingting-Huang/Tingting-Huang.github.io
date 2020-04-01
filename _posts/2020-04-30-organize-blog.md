---
layout: post
title:  "重整博客点点滴滴"
subtitle:   "organize my blog"
date:   2020-02-18 20:02:54
categories: 
tags: 
---

* content
{:toc}



## 1 注册GitHub账号并fork模板

* 



```Your site is published at https://tingting-huang.github.io/```

>注意：如果出现```The CNAME is already taken.``` 莫慌，点击<>code 找到CNAME文件删除即可。

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/delete_cname.jpg)
## 2 jekyll搭建过程
### 2.1 安装Ruby


>注意：以上都是在windows的命令提示符中操作，以下则是在git工具中

## 3 修改博客并远程到GitHub
### 3.1 clone仓库到本地

```git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git``` 
### 3.2 clone仓库文档详细说明
```_config.yml``` 博客配置文档（包括博客标题、favicon、博主 ID、头像、描述、联系方式等基本信息都在这个文档添加或修改）；

## QUESTIONS:

1.使用git push origin master的时候，提示我fatal: unable to access 'https://XXXX@github.com/XXX/XXX' Failed connect to github.com:8087; No error

解决：取消代理，详见[知乎yun liu](https://www.zhihu.com/question/26954892)

2.每次push都需要输入用户名和密码

解决：设置SSH密钥，详见[segmentfault西山雨](https://segmentfault.com/a/1190000002645623#comment-area)

3.设置好SSH后push出现如下情况
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/pusherror.png)或者GitHub总是发邮件通知```“You have an error on line 12(ie., url) of your '_config.yml'”```

解决：修改两处url， url = git@github.com:Yourname/Yourname.github.io.git

a.修改clone到本地的目录/_config.yml中的url；

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/修改_config.yml.png)

b.修改clone到本地的目录/.git/config中的url。

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/修改git下的config.png)


