---
title: Charles抓包工具实战
date: '2022-8-3 10:58:00'
description: '目标:1. 能够用Charles来分析前后端的问题;2. 能够用Charles模拟弱网测试;3. 能使用Charles的断点构建异常的测试场景'
cover: 'https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/10(1).webp'
categories:
  - - Charles
  - - 抓包工具
tags:
  - Charles来分析前后端的问题
  - Charles模拟弱网测试
  - Charles的断点构建异常的测试场景
abbrlink: db3acede
---

# Charles抓包工具实战

课程目标:

1. 能够用Charles来分析前后端的问题
2. 能够用Charles模拟弱网测试
3. 能使用Charles的断点构建异常的测试场景

课程介绍:

1. Charles简介
2. Charles安装与配置
3. Charles实战

## Charles简介

### Charles是什么?

Charles中文名叫青花瓷,它是一款基于http协议的代理服务器,通过成为电脑或者浏览器的代理,然后截取请求和请求结果达到分析抓包的目的.

特点:跨平台(Windows上可以用,Linux上也可以用)、半免费(有免费版本和收费版本,免费版本启动等待10秒,使用半小时自动退出)

### Charles的工作原理?

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/Charles%E7%9A%84%E5%B7%A5%E4%BD%9C%E5%8E%9F%E7%90%86.png)

前置步骤:

1. 需要运行Charles并配置代理
2. 在客户端上面需要配置代理

步骤:

1. 由客户端发送请求
2. Charles接收再发送给服务器
3. 服务器返回请求结果给Charles
4. 由Charles转发给客户端

### Charles能做什么?

1. 支持HTTP及HTTPS代理
2. 支持流量控制
3. 支持接口并发请求
4. 支持重发网络请求
5. 支持断点调试

### Charles的优点?

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/Charles%E7%9A%84%E4%BC%98%E7%82%B9.png)

## Charles的安装和配置

### 下载

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/Charles%E4%B8%8B%E8%BD%BD1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/Charles%E4%B8%8B%E8%BD%BD2.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/Charles%E4%B8%8B%E8%BD%BD3.png)

### 安装

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/Charles%E5%AE%89%E8%A3%85.png)

### Charles组件介绍

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%BB%84%E4%BB%B61.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%BB%84%E4%BB%B62.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%BB%84%E4%BB%B63.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%BB%84%E4%BB%B64.png)

### 配置

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E9%85%8D%E7%BD%AE1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AE%BF%E9%97%AE%E6%8E%A7%E5%88%B6.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/Windows%E4%BB%A3%E7%90%86%E8%AE%BE%E7%BD%AE1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/Windows%E4%BB%A3%E7%90%86%E8%AE%BE%E7%BD%AE%202.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/macos1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/macos2.png)

该方法是:Charles安装再windows上抓取macos的包

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/macos3.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/ip.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/ip1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/macos5.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%89%8B%E6%9C%BA%E4%BB%A3%E7%90%86.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%89%8B%E6%9C%BA.png)

## Charles实战

1. 问题分析
2. https抓包
3. 弱网测试
4. 断点调试

如果所抓取的包和Charles在同一台电脑上只需做如下配置即可

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/win%E9%85%8D%E7%BD%AE.png)

### 问题分析

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AE%9A%E4%BD%8D%E9%97%AE%E9%A2%98.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AE%9A%E4%BD%8D%E9%97%AE%E9%A2%982.png)

### https抓包

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E4%B9%B1%E7%A0%81.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%81%E4%B9%A6.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/windows%E8%AF%81%E4%B9%A6.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E4%BB%A3%E7%90%86%E9%85%8D%E7%BD%AE.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%81%E4%B9%A6%E9%85%8D%E7%BD%AE1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E4%BB%A3%E7%90%86%E9%85%8D%E7%BD%AE1.png)

上图为代理配置的快捷键

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%81%E4%B9%A62.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%81%E4%B9%A63.png)

### Charles流量配置

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%B5%81%E9%87%8F%E9%85%8D%E7%BD%AE.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%B5%81%E9%87%8F%E9%85%8D%E7%BD%AE2.png)

参数:

1. Bandwidth:带宽,代表上行(请求)和下行(响应)速度
2. Utilisation:带宽可用率,大部分选择100%
3. Round-trip latency:请求延时,即每发送一个请求需要延时多久
4. MTU:最大传输单元,即TCP包最大的size,真实模拟TCP层,每次传输的分包情况
5. Reliability:连接可靠性
6. Stability:连接稳定性,用于模拟移动网络

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%BC%B1%E7%BD%91%E6%B5%8B%E8%AF%95.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%BC%B1%E7%BD%91%E6%B5%8B%E8%AF%951.png)

该图为正常运行的时间

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%BC%B1%E7%BD%91%E6%B5%8B%E8%AF%952.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%BC%B1%E7%BD%91%E6%B5%8B%E8%AF%953.png)

该图为模拟弱网测试的一个运行时间

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%BC%B1%E7%BD%91%E6%B5%8B%E8%AF%954.png)

### Charles断点配置

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%96%AD%E7%94%B5%E9%85%8D%E7%BD%AE1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%96%AD%E7%94%B5%E9%85%8D%E7%BD%AE2.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%96%AD%E7%82%B9%E8%B0%83%E8%AF%95%E4%BE%8B%E5%AD%90.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%B7%E6%B1%821.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%B7%E6%B1%822.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%B7%E6%B1%823.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%BB%93%E6%9E%9C.png)





















