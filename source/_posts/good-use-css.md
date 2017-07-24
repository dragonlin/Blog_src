---
title: 一些工作中常用的CSS
date: 2017-07-11 08:50:18
categories: css
---

尝试整理和集合工作中经常遇到的css小技巧...


### 单行超出省略字
```
.div{
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap; 
}
```

### placeholder颜色
```
input::-webkit-input-placeholder{
  color: #666;
}
```
<!--more--> 
### 禁止文本选择
```
.div{
  -moz-user-select:none;
  -webkit-user-select:none;
  -ms-user-select:none;
  -khtml-user-select:none;
  user-select:none;
}
```

### 表单100%宽，但是有padding
```
input{
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
```


### 横向滚动
```
.div{
  white-space: nowrap;
  overflow-x: auto;
  overflow-y: hidden;
}
```

## 不断更新