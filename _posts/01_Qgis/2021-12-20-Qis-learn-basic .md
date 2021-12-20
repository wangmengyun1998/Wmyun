---
title: QGIS_02_界面介绍
tags:
  - Qgis
  - Python
---

[油管视频](https://www.youtube.com/watch?v=Eg4_duqH5Q4 )   
点击[这里](https://qgis.org/en/site/forusers/download.html)下载安装Qgis，一路默认安装就可以了，**注意Qgis安装路径不要有中文，要不然容易出错**。
<!--more-->
## 1-1 初识界面
**1.Qgis中文界面的设置如下所示** 

![]({{site.url}}/theme/img/2.png)

<!-- <img src="{{site.url}}/theme/img/2.png">  -->

**2.我一开始的界面是这样的**  

<img src="{{site.url}}/theme/img/3.png" >   
 
点击`View`->`Panels`、`Toolbars`,可在页面中添加`Browser`、`Layers`等

<img src="{{site.url}}/theme/img/4.png" >  

我们就从下面这个界面开始Qgis  

<img src="{{site.url}}/theme/img/5.png" >   

当然，按住Browser可以拖动到不同地方。  

**3.加载底图，  在`Browser`->  `XYZ Tiles`->`OpenStreetMap`->`Add Layers to Project`,即可将地图加载进去，在`Layers`中，可以看到刚加载进来的`OpenStreetMap` ,右击`Remove Layer...` ，即可删除图层** 

<img src="{{site.url}}/theme/img/6.png" >   
<img src="{{site.url}}/theme/img/7.png" >   

接下来我们添加shp文件（保证自己的本地上有shp文件），有三种方式：  
**第一种**：在`Browser`界面可以看到本次路径，找到你存放shp的路径即可，在`Layers`中可以看到加载进来的shp 

<img src="{{site.url}}/theme/img/8.png" >   
<img src="{{site.url}}./theme/img/9.png" >     
 
 **第二种**：在左侧找到`Vector`->在`Source`下找到shp文件路径，最后点击`Add`
 
<img src="{{site.url}}/theme/img/10.png" >   

如果左侧没有`Vector`,依次点击`View`->`Toolbars`->`Manage Layers Toolbar`即可在左侧显示
  
**第三种**:点击`Layers`->`Data Source Manager`,在找到`Vector`->在`Source`下找到shp文件路径，最后点击`Add`即可  

<img src="{{site.url}}/theme/img/11.png" >   
<img src="{{site.url}}/theme/img/12.png" >

**4.在用第二种、第三种加载shp时，会遇到下面的几个文件，那么shp、shx、dbf、prj、xml都是什么文件、都有什么作用?**        
Shapefile使用点、线、多边形存储要素的形状，具有简单、快速显示的优点；缺点是不能存储拓扑关系。一个shapefile是由若干个文件组成的，空间信息和属性信息分离存储，所以称之为“基于文件”的GIS数据格式。

每个shapefile，都至少有这三个文件组成，其中：

- *.shp文件，存储的是几何要素的的空间信息，也就是XY坐标；
- *.shx文件，存储的是有关*.shp存储的索引信息。它记录了在*.shp中，空间数据是如何存储的，XY坐标的输入点在哪里，有多少XY坐标对等信息；
- *.dbf文件，存储地理数据的属性信息的dBase表。  

这三个文件是构成一个shapefile的基本文件，shapefile还可以有其他一些文件，但所有这些文件都与该shapefile同名，并且存储在同一路径下。
其它较为常见的文件：
- *.prj文件，如果shapefile定义了坐标系统，那么它的空间参考信息将会存储在*.prj文件中；
- *.shp.xml文件，这是对shapefile进行元数据浏览后生成的xml元数据文件；
- *.sbn文件和*.sbx文件，这两个存储的是shapefile的空间索引，它能加速空间数据的读取。这两个文件是在对数据进行操作、浏览或连接后才产生的  

虽然Shapefile无法存储拓扑关系，但它并不仅仅是普通用于显示的图形文件，作为地理数据，它自身是有拓扑的。比如一个多边形要素类，shapefile会按顺时针方向为它的所有顶点排序，然后按顶点顺序两两连接成的边线向量，在向量右侧的为多边形的内部，在向量左侧的是多边形的外部。
<img src="{{site.url}}/theme/img/13.png" >  

**5.在`Layers`中右击导入的shp，点击`Open Attribute Table`,可以看到一些属性信息**

<img src="{{site.url}}/theme/img/14.png" >

