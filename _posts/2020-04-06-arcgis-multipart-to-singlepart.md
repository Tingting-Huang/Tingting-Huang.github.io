---
layout: post
title:  "ArcGIS将一个图层中的多个要素分别输出为单个图层"
subtitle:   
date:   2020-04-06 17：00
categories: ArcGIS feature
tags: ArcGIS feature multipart singlepart
---

* content
{:toc}

实例：某流域图层中包含306个小流域面要素，现将其拆分成306个单独的图层。

工具：ArcGIS 10.1->Data Management Tools->Features->Multipart to Singlepart

#### 1. 选择ModelBuilder添加feature selection和Multipart to Singlepart；
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/20200406162916.jpg)
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/20200406162925.jpg)

#### 2. selected features和Multipart to Singlepart加入连接，并设置某流域图层为input features；
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/20200406163404.jpg)

#### 3.feature selection设置拆分字段，“流域编号”；Multipart to Singlepart设置输出文件名，%Value%表示根据拆分字段的数值进行文件命名；
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/20200406163020.jpg)
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/20200406164240.jpg)

#### 4. 总的model流程及结果。
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/20200406163106.jpg)
![](https://raw.githubusercontent.com/tingting-huang/PicGo/master/blog_files/img/PicGo-GitHub-PicBed/20200406163027.jpg)


