---
title: Cdn-Libs cdn公共库加速资源汇总
categories:
  - 技|工作技巧
tags:
  - cdn
date: 2017-02-20 15:31:09
---

　　CDN公共库是指将常用的JS库存放在CDN节点，以方便广大开发者直接调用。与将JS库存放在服务器单机上相比，CDN公共库更加稳定、高速。一般的CDN公共库都会包含全球所有最流行的开源JavaScript库，你可以在自己的网页上直接通过script标记引用这些资源。这样做不仅可以为您节省流量，还能通过CDN加速，获得更快的访问速度。

　　*注意网站要支持ssl的有些资源慎用。*

<div align="center">
{% qnimg cdnlib.jpg title:CDN公共库 alt:CDN公共库 'class:class1 class2'  extend:?imageView2/2/w/300 %}</div>

<!-- more --> 

### bootcdn
<div align="center">
{% qnimg cdnbootcdn.jpg title:bootcdn alt:bootcdn 'class:class1 class2' extend:?imageView2/2/w/600 %}</div>
bootcdn 第一，很齐全。
```
http://www.bootcdn.cn/
```
很赞


### 新浪前端cdn库
```
http://lib.sinaapp.com/
```
　　（推荐，多年了一直坚挺）
　　新浪云计算是新浪研发中心下属的部门，主要负责新浪在云计算领域的战略规划，技术研发和平台运营工作。主要产品包括 应用云平台Sina App Engine（简称SAE）。
SAE的CDN节点覆盖全国各大城市的多路（电信、联通、移动、教育）骨干网络，使开发者能够方便的使用高质量的CDN服务

### 七牛云存储 开放静态文件CDN
　　七牛云存储提供一个尽可能全面收录优秀开源库的仓库，并免费提供 CDN 加速服务。
```
官网：http://www.staticfile.org/
```

### 百度静态资源公共库 
　　百度公共CDN为站长的应用程序提供稳定、可靠、高速的服务，包含全球所有最流行的开源JavaScript库。
　　百度静态资源公共库，`http://cdn.code.baidu.com/`

### Bootstrap中文网开源项目免费 
　　Bootstrap中文网开源项目免费的CDN服务，`http://www.bootcdn.cn/`
这个也比较全，非常不错，甚至可以找到其他cdn没有的比如doT.js 

### 外国cdnjs
```
https://cdnjs.com/
```
　　CDNJS应该算是最完整的的JS库了。存储了大部分主流的 JS 库，甚至 CSS、image 和 swf，不过很多国内优秀开源库是没有的。很多国外前卫的Js库在CDNJS大都能找到。

### Microsoft ASP.net CDN
　　ASP.NET开发团队推出的一个新的微软Ajax CDN（Content Delivery Network，内容分发网络）服务，该服务提供了对AJAX库（包括jQuery 和 ASP.NET AJAX）的缓存支持。该服务是免费的，不需任何注册，可用于商业性或非商业性用途。
```
官网：http://www.asp.net/ajaxlibrary/cdn.ashx
```
　　Ps：微软出品，自然不会太差。虽然在天朝，速度依然不会太慢（当然比不上国内的其他cdn）。

### jsDelivr 
　　jsDelivr是基于MaxCDN的一个免费开源的 CDN 解决方案，用于帮助开发者和站长。jsDelivr包含 JavaScript 库、jQuery 插件、CSS 框架、字体等等 Web 上常用的静态资源。
```
官网：http://www.jsdelivr.com/
```

### 注意事项
　　当然，用别人的 CDN 都是不保险的，所以建议在 CDN 读取失败的时候从自己服务器提供：
```
<script src="//http://lib.sinaapp.com/js/jquery/1.7.2/jquery.min.js"></script>
<script>
if (!window.jQuery) {
var script = document.createElement('script');
script.src = "/js/jquery.min.js";
document.body.appendChild(script);
}
</script>
```

