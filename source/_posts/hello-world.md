---
title: Hello World
date: 2017-07-09 09:30:00
tags: 
  - hexo
categories: Hexo
---
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start
### Create a new post
``` bash
$ hexo new "My New Post"
```
More info: [Writing](https://hexo.io/docs/writing.html)
### Run server
``` bash
$ hexo server
```
More info: [Server](https://hexo.io/docs/server.html)

<!--more--> 

### Generate static files
``` bash
$ hexo generate
```
More info: [Generating](https://hexo.io/docs/generating.html)
### Deploy to remote sites
``` bash
$ hexo deploy
```
More info: [Deployment](https://hexo.io/docs/deployment.html)

## 标签和分类

``` html
---
title: My New Post
date: 2017-07-09 18:57:13
tags: 
  - tag1
  - tag2
categories: xxx
---
```
冒号后面要有空格 --好像不一定要有空格 可以没有
应该在 ---之上，---下面是页面内容
令：要添加tags和categories页面；且主题的配置文件和站点的配置文件tags和categories的注释要打开
### 添加标签
``` bash
$ hexo new page tags
```
确认站点配置文件里有tag_dir: tags
确认主题配置文件里有tags: /tags
编辑站点的source/tags/index.md，添加

``` json
title: tags
date: 2017-07-09 18:39:01
type: "tags"
comments: false
```

### 添加分类

``` bash
$ hexo new page categories
```
确认站点配置文件里有category_dir: categories
确认主题配置文件里有categories: /categories
编辑站点的source/categories/index.md，添加
``` json
title: categories
date: 2017-07-09 18:47:06
type: "categories"
comments: false
```