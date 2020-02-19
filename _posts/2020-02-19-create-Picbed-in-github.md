---
layout: post
title:  "Github+PicGO搭建图床"
subtitle:   ""
date:   2020-02-19 20:02:54
categories: github 
tags: github Picgo
---

* content
{:toc}

几个月前吧，突然一阵抽风，想搭建个博客来记录自己的生活学习种种，当时搞了半天没成功就不了了之了。最近借着疫情闲赋在家的空档，顺着[xudailong_blog](https://blog.csdn.net/xudailong_blog/article/details/78762262)的思路，选择了在github上用jekyll搭建博客。尽管网上很多人写过类似教程，但软件更新换代较快，所以中途走了无数的弯路，希望这篇博文能对看到的你们有所帮助。因本人纯属小白，相关术语并不进行解释，直接上操作步骤。

## 1 注册GitHub账号并fork模板

* 注册账号，我相信你们都会；

* 新建一个repository仓库，例如命名“a"；

* fork[徐代龙模板](https://github.com/xudailong/xudailong.github.io);

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/fork.jpg)

* 进入settings修改repository name，这个仓库名一定要与“a”一致；

* 下拉到GitHub Pages,点击以下此链接即可进入你的博客；

```Your site is published at https://tingting-huang.github.io/```

>注意：如果出现```The CNAME is already taken.``` 莫慌，点击<>code 找到CNAME文件删除即可。

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/delete_cname.jpg)
## 2 jekyll搭建过程
### 2.1 安装Ruby
* [ruby官网](https://rubyinstaller.org/downloads/) 下载，建议选择2.6.5 with devkit版本，一路默认安装，同时注意勾选MSYS2相关的;

* win+R输入cmd进入命令提示符，```ruby -v``` 得到ruby版本号，即安装成功.

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/ruby_v.jpg)
### 2.2 安装RubyGems
* [rubygems官网](https://rubygems.org/pages/download)下载，版本选择3.0.6； 

* cd到RubyGems目录；   

* 在rubygems目录下输入```ruby setup.rb``` 安装；   

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/安装rubygems.png) 
### 2.3 用RubyGems安装Jekyll
* 在初始默认目录即C:\users\下输入``` gem install jekyll``` 安装；   

* 安装结束画面，至此jekyll就已经安装完毕。

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/jekyll安装成功.png)
### 2.4 创建博客本地存放空间
* D盘新建一个文件夹，命名如jekyllWorkspace;

* cd到jekyllWorkspace;   

* 执行jekyll new "yourname"创建新的工作区;   

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/jekyllnew_tt.jpg)

* 文件结构如下;

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/本地文件结构.png)

* cd到博客文件夹，输入```jekyll serve --watch``` 开启服务器   

* 启动服务器成功
* 
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/启动服务器watch.png)


>注意：以上都是在windows的命令提示符中操作，以下则是在git工具中

## 3 修改博客并远程到GitHub
### 3.1 clone仓库到本地
* sock5仅代理GitHub加速clone（能健康上网的前提下），参考[知乎汪小九](https://www.zhihu.com/question/27159393)

```git config --global http.https://github.com.proxy socks5://127.0.0.1:10808```

* 选择clone博客存放文件夹，如果不修改，默认C:\users\123，pwd查看当前默认文件夹；

* clone博客到本地

```git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git``` 
### 3.2 clone仓库文档详细说明
```_config.yml``` 博客配置文档（包括博客标题、favicon、博主 ID、头像、描述、联系方式等基本信息都在这个文档添加或修改）；

```index.html``` 博客架构文档；

```_includes``` 博客调用的网页模块（比如导航栏、底栏、博文内容显示、评论模块等），一般不需要管；

```_layouts``` 存放博客调用的页面模板文件（比如博客主页、具体博文页）的文件夹；

```css``` 存放博客系统的页面渲染文档文件夹，主要用于调节诸如标题字体、博文字体大小颜色之类；

```js``` 存放博客调用的 JS 文档文件夹；

```_posts``` 博客正文存放的文件夹。命名有规定，必须为「日期 + 标题」的模式，即「2015-04-27-Like-Kissing.md」，才能发布到博客里；

```images``` 图片文件夹，存放博客相关素材，包括博客 favicon、博主头像等图片及博文贴图素材；

```CNAME``` 用于绑定个人域名的文档；

```404.html``` 「404 Not Found.」站点链接无法访问时的提示页面；

```About.html``` 博客中的个人说明文档（About Me），以 html、md 格式为主；

```feed.xml``` 博客的 RSS 订阅；

```README.md``` 项目说明文档。用于 Github 个人项目主页的说明（描述）。

除此之外，还有诸如 ```fonts``` 文件夹，存放博客用的字体文件，或有主题是将 ```css/js/fonts/images``` 等文件夹合并到 ```_assets``` 为名的主文件夹中。```404.html/feed.xml/CNAME``` 文件并非必须，但一般架构完整的博客都有。

说明引自[MartinGuo](https://martinguo.github.io/blog/2015/10/19/Build-Your-First-GitHub-Pages-Blog/)
### 3.3 本地修改/撰写博客并上传到GitHub
* 下载安装markdown，日后写博文用。详见[简书今夜相思又几许](https://www.jianshu.com/p/5604996dcdbb)

* 在_posts目录下新建一个markdown文件，头信息必须在文件的开始部分，且按照 YAML 的格式写在两行三虚线之间

layout: post

title:  "Welcome to Jekyll!"

date:   2018-03-31 02:36:26 +0800

tags:

categories：


* ```git status```查看文件状态

* ```git add --all```  or  ```git add .```将文件add到本地缓冲区

* ```git commit -m "Update filename"```查看修改内容; 

* ```git push origin master```  or  ```git push origin master -f```提交push博文到远程自己的项目分支库,后加-f表示强行提交;

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


