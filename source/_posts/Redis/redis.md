---
title: Redis介绍
date: '2022-8-3 17:58:00'
description: >-
  学习目标:1. 了解nosql与redis;2. 了解redis五种数据类型string,hash,list,set,zset;3.
  了解redis五种数据类型的增,删,改,查操作.
cover: 'https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/19.webp'
categories:
  - - 数据库
tags:
  - Redis
abbrlink: 873fa4d3
---

# redis

学习目标:

1. 了解nosql与redis
2. 了解redis五种数据类型string,hash,list,set,zset
3. 了解redis五种数据类型的增,删,改,查操作.

## NoSQL简介

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/nosql%E7%AE%80%E4%BB%8B.png)

## redis简介

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/redis%E7%AE%80%E4%BB%8B.png)

## redis基本操作

1. 启动服务端:redis-server
2. 启动客户端(默认redis客户端不能正确显示中文):redis-cli   
3. 启动客户端(用下面命令启动客户端,可以正确显示中文):redis-cli --raw (--raw前边要有空格,前面的两个之间是不需要空格的)
4. 运行测试命令:ping  (只需写ping即可,将收到PONG,即表示连到服务器)

## 切换数据库

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%87%E6%8D%A2%E6%95%B0%E6%8D%AE%E5%BA%931.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%87%E6%8D%A2%E6%95%B0%E6%8D%AE%E5%BA%932.png)

## redis键值对说明

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/redis%E9%94%AE%E5%80%BC%E5%AF%B9%E8%AF%B4%E6%98%8E.png)

## 字符串操作

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AD%97%E7%AC%A6%E4%B8%B2%E6%93%8D%E4%BD%9C1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AD%97%E7%AC%A6%E4%B8%B2%E6%93%8D%E4%BD%9C2.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AD%97%E7%AC%A6%E4%B8%B2%E6%93%8D%E4%BD%9C3.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AD%97%E7%AC%A6%E4%B8%B2%E6%93%8D%E4%BD%9C4.png)

## 获取

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%8E%B7%E5%8F%961.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%8E%B7%E5%8F%962.png)

## 删除

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%A0%E9%99%A41.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%A0%E9%99%A42.png)

## 健命令

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%81%A5%E5%91%BD%E4%BB%A41.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%81%A5%E5%91%BD%E4%BB%A42.png)

## 判断健是否存在

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%A4%E6%96%AD%E5%81%A51.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%A4%E6%96%AD%E5%81%A52.png)

## 查看健对应的value类型

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%9F%A5%E7%9C%8B%E5%81%A51.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%9F%A5%E7%9C%8B%E5%81%A52.png)

## 设置已有健的过期时间

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%81%A5%E8%BF%87%E6%9C%9F1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%81%A5%E8%BF%87%E6%9C%9F2.png)

## 查看健有效时间

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%9F%A5%E7%9C%8B%E5%81%A5%E6%9C%89%E6%95%88%E6%97%B6%E9%97%B4.png)

## 哈希 hash

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/hash%E4%BB%8B%E7%BB%8D.png)

## 哈希操作

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%93%88%E5%B8%8C%E6%93%8D%E4%BD%9C1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%93%88%E5%B8%8C%E6%93%8D%E4%BD%9C2.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%93%88%E5%B8%8C%E6%93%8D%E4%BD%9C3.png)

## 获取

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%8E%B7%E5%8F%9611.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%8E%B7%E5%8F%9612.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%8E%B7%E5%8F%9613.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%8E%B7%E5%8F%9614.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%8E%B7%E5%8F%9615.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%8E%B7%E5%8F%9616.png)

## 删除

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%A0%E9%99%A411.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%A0%E9%99%A412.png)

## 列表list

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/list1.png)

前面三种总结

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/string%E5%9B%BE.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%93%88%E5%B8%8C%E5%9B%BE.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%97%E8%A1%A8%E5%9B%BE.png)

## 增加

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/list%E5%A2%9E%E5%8A%A01.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/list%E5%A2%9E%E5%8A%A02.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/list%E5%A2%9E%E5%8A%A03.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/list%E5%A2%9E%E5%8A%A04.png)

## 获取

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/list%E8%8E%B7%E5%8F%961.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/list%E8%8E%B7%E5%8F%962.png)

## 修改

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/list%E4%BF%AE%E6%94%B91.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/list%E4%BF%AE%E6%94%B92.png)

## 删除

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/list%E5%88%A0%E9%99%A41.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/list%E5%88%A0%E9%99%A42.png)

## 无序集合set

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%97%A0%E5%BA%8F%E9%9B%86%E5%90%881.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%97%A0%E5%BA%8F%E9%9B%86%E5%90%882.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%97%A0%E5%BA%8F%E9%9B%86%E5%90%883.png)

## 获取

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%97%A0%E5%BA%8F%E5%88%97%E8%A1%A8%E8%8E%B7%E5%8F%961.png)

## 删除

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%97%A0%E5%BA%8F%E9%9B%86%E5%90%88%E5%88%A0%E9%99%A4.png)

## 有序集合zset

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/zset1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/zset2.png)

## 增加

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/zset%E5%A2%9E%E5%8A%A01.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/zset%E5%A2%9E%E5%8A%A02.png)

## 获取

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/zset%E8%8E%B7%E5%8F%961.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/zset%E8%8E%B7%E5%8F%962.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/zset%E8%8E%B7%E5%8F%963.png)

## 删除

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/zset%E5%88%A0%E9%99%A4.png)













