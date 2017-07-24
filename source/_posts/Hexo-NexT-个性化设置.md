---
title: 'Hexo-NexT:个性化设置'
date: 2017-07-23 13:39:21
categories: Hexo
---

### 1. 添加背景动画

在<font color='red'>\themes\next\\_config.yml</font>中添加以下字段开启此功能：

```
# Canvas-nest
canvas_nest: true
```

添加完了，发现博客背景是白色，会遮住动画，只留下两边一点点的位置看到动画效果，这时候可以去设置一下背景颜色，在<font color='red'>\themes\next\source\css\\_schemes\Pisces\_layout.styl</font>中，把.content-wrap中的 <font color='red'>background</font> 修改为none。

### 2. 添加音乐

随便找了一首歌：http://music.163.com/#/outchain/2/436514254/m/use/html
html 代码如下
```
<iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=330 height=86 src="//music.163.com/outchain/player?type=2&id=436514254&auto=1&height=66"></iframe>
```
打开目录<font color='red'>\themes\next\layout\\_custom\header.swig</font>
copy 上述代码,done.

<!--more-->
### 3. 添加High一下
打开博客根目录 <font color='red'> \themes\next\layout\\_partials\header.swig </font> ,在
\<ul\>... /ul>标签之间加入以下代码：

```
<li> <a title="把这个链接拖到你的Chrome收藏夹工具栏中" href='javascript:(function() {
    function c() {
        var e = document.createElement("link");
        e.setAttribute("type", "text/css");
        e.setAttribute("rel", "stylesheet");
        e.setAttribute("href", f);
        e.setAttribute("class", l);
        document.body.appendChild(e)
    }
    function h() {
        var e = document.getElementsByClassName(l);
        for (var t = 0; t < e.length; t++) {
            document.body.removeChild(e[t])
        }
    }
    function p() {
        var e = document.createElement("div");
        e.setAttribute("class", a);
        document.body.appendChild(e);
        setTimeout(function() {
            document.body.removeChild(e)
        }, 100)
    }
    function d(e) {
        return {
            height : e.offsetHeight,
            width : e.offsetWidth
        }
    }
    function v(i) {
        var s = d(i);
        return s.height > e && s.height < n && s.width > t && s.width < r
    }
    function m(e) {
        var t = e;
        var n = 0;
        while (!!t) {
            n += t.offsetTop;
            t = t.offsetParent
        }
        return n
    }
    function g() {
        var e = document.documentElement;
        if (!!window.innerWidth) {
            return window.innerHeight
        } else if (e && !isNaN(e.clientHeight)) {
            return e.clientHeight
        }
        return 0
    }
    function y() {
        if (window.pageYOffset) {
            return window.pageYOffset
        }
        return Math.max(document.documentElement.scrollTop, document.body.scrollTop)
    }
    function E(e) {
        var t = m(e);
        return t >= w && t <= b + w
    }
    function S() {
        var e = document.createElement("audio");
        e.setAttribute("class", l);
        e.src = i;
        e.loop = false;
        e.addEventListener("canplay", function() {
            setTimeout(function() {
                x(k)
            }, 500);
            setTimeout(function() {
                N();
                p();
                for (var e = 0; e < O.length; e++) {
                    T(O[e])
                }
            }, 15500)
        }, true);
        e.addEventListener("ended", function() {
            N();
            h()
        }, true);
        e.innerHTML = " <p>If you are reading this, it is because your browser does not support the audio element. We recommend that you get a new browser.</p> <p>";
        document.body.appendChild(e);
        e.play()
    }
    function x(e) {
        e.className += " " + s + " " + o
    }
    function T(e) {
        e.className += " " + s + " " + u[Math.floor(Math.random() * u.length)]
    }
    function N() {
        var e = document.getElementsByClassName(s);
        var t = new RegExp("\\b" + s + "\\b");
        for (var n = 0; n < e.length; ) {
            e[n].className = e[n].className.replace(t, "")
        }
    }
    var e = 30;
    var t = 30;
    var n = 350;
    var r = 350;
    var i = "//7xuupy.com1.z0.glb.clouddn.com/tongxingSibel%20-%20Im%20Sorry.mp3";
    var s = "mw-harlem_shake_me";
    var o = "im_first";
    var u = ["im_drunk", "im_baked", "im_trippin", "im_blown"];
    var a = "mw-strobe_light";
    var f = "//s3.amazonaws.com/moovweb-marketing/playground/harlem-shake-style.css";
    var l = "mw_added_css";
    var b = g();
    var w = y();
    var C = document.getElementsByTagName("*");
    var k = null;
    for (var L = 0; L < C.length; L++) {
        var A = C[L];
        if (v(A)) {
            if (E(A)) {
                k = A;
                break
            }
        }
    }
    if (A === null) {
        console.warn("Could not find a node of the right size. Please try a different page.");
        return
    }
    c();
    S();
    var O = [];
    for (var L = 0; L < C.length; L++) {
        var A = C[L];
        if (v(A)) {
            O.push(A)
        }
    }
    })()    '>High一下</a> </li>
```

### 4. 添加点击💗 样式

1. 将 [love.js](https://github.com/dragonlin/dragonlin.github.io/tree/master/js/src) 文件添加到 <font color='red'>\themes\next\source\js\src</font> 文件目录下。
2. 找到 <font color='red'>\themes\next\layout\\_layout.swing</font> 文件， 在文件的后面，</body> 标签之前 添加以下代码：
```
<!-- 页面点击小红心 -->
<script type="text/javascript" src="/js/src/love.js"></script>
```

### 5. 为博客加上GitHub丝带

如果是Next主题（其他主题也差不多），添加GitHub丝带：在<font color='red'>themes\next\layout\\_layout.swig</font> 中加入相关代码，记得修改自己的链接。

相关代码你可以在GitHub官方网站[GitHub Ribbons](https://github.com/blog/273-github-ribbons)上进行选择。

### 6.添加Local Search功能

安装 hexo 插件

在你的站点文件夹中，用shell等运行下面这行代码：
```
$ npm install hexo-generator-searchdb --save
```

启用本地搜索

编辑主题配置文件启用本地搜索
```
# Local search
local_search:
  enable: true
```

编辑站点配置文件 添加以下字段：
```
search:
  path: search.xml
  field: post
  format: html
  limit: 10000
```

### 7. 自定义more

这里开始使用markdown格式输入你的正文。 
```
<!--more--> 
#more标签以下的内容要点击“阅读全文”才能看见
#more标签以上的内容为你首页显示文章的摘要部分
```

### 8. 头像👦动画效果

试试吧
```
.site-author-image {
    border-radius: 100%;
    animation: cycle 2s 0.5s forwards;
    transition: border-radius 2s;
}
.site-author-image:hover {
    border-radius: 0;
    border: 2px solid #0ff;
}
```