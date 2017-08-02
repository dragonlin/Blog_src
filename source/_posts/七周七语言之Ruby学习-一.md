---
title: 七周七语言之Ruby学习(一)
date: 2017-07-23 07:17:45
tags: 
  - 七周七语言
  - Ruby
  - Mac
categories: Ruby
---
## 查看版本
> ruby -v

在Mac打开终端输入 <code>irb</code> 进入命令行环境
## 打印函数puts
```
irb(main):003:0> puts 'hello world'
hello world
=> nil
```
## 单引号不会做字符串替换，只有双引号才会做字符串替换
```
irb(main):004:0> language = 'ruby'
=> "ruby"
irb(main):005:0> puts 'hello,#{language}'
hello,#{language}
=> nil
irb(main):006:0> puts "hello,#{language}"
hello,ruby
=> nil
```
## exit 退出命令行环境

## 查看类型
```
irb(main):002:0> 4.class
=> Fixnum
```

# 习题
