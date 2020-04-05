---
layout: post
title:  "word图表添加索引"
subtitle:   
date:   2020-04-03 23：50
categories: word 
tags: word figure index 
---

* content
{:toc}


#### 1. 确保所有图片为嵌入式；
毕业论文要求正文行距为20磅，插入图片时会不完全显示，更改行距即可解决。
单击图片，更改行距为1.5倍，无首行缩进，创建为“图片”样式。

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/0嵌入式.jpg)

#### 2. 在图下方插入题注；
因为我的是顺序编号，直接默认即可；如果是按章节编号，则选择“编号->题注编号”勾选“包含章节号”。

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/1插入题注.png)
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/2包含章节.png)

#### 3. 复制生成的题注，即“图1”（默认是图表1，我去掉了表字），CTRL+H，在替换框中的查找内容输入：^g，替换为输入：^&^p^c，然后全部替换。
^g是每一张图片，^&是搜索的原对象，^g替换成^&表示N个图都保持原样不替换。^p是换行，表示题注位于图片的下一行，^c表示复制的内容。

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/20200405101541.jpg)

![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/4.2替换aa.jpg)
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/4.3拒绝从头搜索.jpg)
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/4.4两个图1.jpg)

#### 4. CTRL+A 全选，然后按fn+F9（有的电脑可能F9）刷新即可自动编号；

#### 5. 插入目录
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/5插入表目录.jpg)