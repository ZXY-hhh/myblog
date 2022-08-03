---
title: MySQL介绍
date: '2022-8-3 17:58:00'
description: >-
  学习目标:1. 掌握navicat基本使用;2. 掌握select基本语法;3. 掌握insert基本语法;4. 掌握update基本语法;5.
  掌握delete基本语法
cover: 'https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/18.webp'
categories:
  - - 计算机基础
  - - 数据库
tags:
  - MYSQL
abbrlink: c5f0c5d0
---

# MySQL

学习目标:

1. 掌握navicat基本使用
2. 掌握select基本语法
3. 掌握insert基本语法
4. 掌握update基本语法
5. 掌握delete基本语法

## navicat连接到MySQL

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/navicat%E8%BF%9E%E6%8E%A5%E5%88%B0mysql.png)

## navicat新建数据库以及查询基本操作

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%89%93%E5%BC%80%E9%93%BE%E6%8E%A5.png)

### 新建数据库

![](D:\黑马测试学习路线\5.mysql\新建数据库1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%96%B0%E5%BB%BA%E6%95%B0%E6%8D%AE%E5%BA%932.png)

### 查询

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%9F%A5%E8%AF%A2%E6%93%8D%E4%BD%9C.png)

## 注释

* 在navicat中按ctrl+/快速注释选中的sql代码
* 在navicat中按ctrl+shift+/选中sql代码取消注释(我的navicat直接ctrl+/即可)

## mysql常用数据类型

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/mysql%E5%B8%B8%E7%94%A8%E6%95%B0%E6%8D%AE%E7%B1%BB%E5%9E%8B1.png)

## 数据库中的元素

数据库---database

表---table

字段---field

记录---record

## 创建表

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%9B%E5%BB%BA%E8%A1%A81.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%9B%E5%BB%BA%E8%A1%A82.png)

## 插入数据

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8F%92%E5%85%A5%E6%95%B0%E6%8D%AE1.png)

## 插入多条记录

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8F%92%E5%85%A5%E5%A4%9A%E6%9D%A1%E8%AE%B0%E5%BD%951.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8F%92%E5%85%A5%E5%A4%9A%E6%9D%A1%E8%AE%B0%E5%BD%952.png)

## Linux上解决navicat试用期

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/navicat%E8%AF%95%E7%94%A8%E6%9C%9F.png)

一直取消取消

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%95%E7%94%A8%E6%9C%9F22.png)

点击使试用即可

navicat的使用在Linux上和Windows上的操作一模一样

如下图片是使用Windows下的navicat连接Linux上的mysql

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%BF%9E%E6%8E%A5.png)

## select查询表

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/select%E6%9F%A5%E8%AF%A2%E8%A1%A8.png)

## update修改数据

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/update%E4%BF%AE%E6%94%B9%E6%95%B0%E6%8D%AE.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E9%80%89%E4%B8%AD%E6%89%A7%E8%A1%8C.png)

在navicat可以选中一条语句单独执行

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/update%E4%BF%AE%E6%94%B9%E6%95%B0%E6%8D%AE2.png)

## delete删除记录

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/delete%E5%88%A0%E9%99%A4%E8%AE%B0%E5%BD%95.png)

## truncate table删除表的数据

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/truncate%E5%88%A0%E9%99%A4%E8%A1%A8%E7%9A%84%E6%95%B0%E6%8D%AE.png)

## delete和truncate的区别

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%8C%BA%E5%88%AB.png)

## 删除表

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%A0%E9%99%A4%E8%A1%A8.png)

## 字段的约束

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AD%97%E6%AE%B5%E7%9A%84%E7%BA%A6%E6%9D%9F.png)

## 主键与自增长

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E4%B8%BB%E9%94%AE.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E4%B8%BB%E9%94%AE3.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E4%B8%BB%E9%94%AE4.png)

## 非空

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E9%9D%9E%E7%A9%BA1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E9%9D%9E%E7%A9%BA2.png)

## 唯一

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%94%AF%E4%B8%80.png)

navicat快捷键执行(ctrl+r)

## 字段的别名

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AD%97%E6%AE%B5%E7%9A%84%E5%88%AB%E5%90%8D.png)

## 表的别名

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%A1%A8%E7%9A%84%E5%88%AB%E5%90%8D.png)

## distinct过滤重复记录

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/distinct.png)

## where子句

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/where%E5%AD%90%E5%8F%A5.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/where%E5%AD%90%E5%8F%A522.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/where%E5%AD%90%E5%8F%A53.png)

## 比较运算符

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%AF%94%E8%BE%83%E8%BF%90%E7%AE%97%E7%AC%A61.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%AF%94%E8%BE%83%E8%BF%90%E7%AE%97%E7%AC%A62.png)

## 课堂练习

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%BE%E5%A0%82;%E7%BB%83%E4%B9%A01.png)

## 逻辑运算符

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E9%80%BB%E8%BE%91%E8%BF%90%E7%AE%97%E7%AC%A61.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E9%80%BB%E8%BE%91%E8%BF%90%E7%AE%97%E7%AC%A62.png)

## 课堂练习

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%BE%E5%A0%82%E7%BB%83%E4%B9%A02.png)

## 模糊查询

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%A8%A1%E7%B3%8A%E6%9F%A5%E8%AF%A2.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%A8%A1%E7%B3%8A%E6%9F%A5%E8%AF%A22.png)

## 课堂练习

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%BE%E5%A0%82%E7%BB%83%E4%B9%A03.png)

## 范围查找

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%8C%83%E5%9B%B4%E6%9F%A5%E6%89%BE.png)

## 课堂练习

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%BE%E5%A0%82%E7%BB%83%E4%B9%A04.png)

## 空判断

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%A9%BA%E5%88%A4%E6%96%AD1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%A9%BA%E5%88%A4%E6%96%AD2.png)

## where子句可以用到update和delete语句后面

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/where%E5%AD%90%E5%8F%A54.png)

## 课后练习

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%BE%E5%90%8E%E7%BB%83%E4%B9%A05.png)

## order by 排序

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8E%92%E5%BA%8F.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8E%92%E5%BA%8F2.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8E%92%E5%BA%8F3.png)

## 聚合函数

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%81%9A%E5%90%88%E5%87%BD%E6%95%B0.png)

## count总记录数

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/count.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/count2.png)

## max最大值

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/max1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/max2.png)

## min最小值

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/min1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/min2.png)

## sum求和

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/sum1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/sum2.png)

## avg求平均数

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/avg1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/avg2.png)

## 数据分组

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%95%B0%E6%8D%AE%E5%88%86%E7%BB%84.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%95%B0%E6%8D%AE%E5%88%86%E7%BB%842.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%95%B0%E6%8D%AE%E5%88%86%E7%BB%843.png)

## having分组聚合之后的筛选

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/having1.png)

## having配合聚合函数的使用

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/having%E9%85%8D%E5%90%88.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/having%E9%85%8D%E5%90%882.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/having4.png)

## limit显示指定的记录数

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/limit1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/limit2.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/limit3.png)

## 数据分页显示

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%86%E9%A1%B51.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%86%E9%A1%B52.png)

## 课堂练习

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%BE%E5%A0%82%E7%BB%83%E4%B9%A05.png)

## 连接查询

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%BF%9E%E6%8E%A5%E6%9F%A5%E8%AF%A21.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%BF%9E%E6%8E%A5%E6%9F%A5%E8%AF%A22.png)

## 内连接

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%86%85%E8%BF%9E%E6%8E%A5.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%86%85%E8%BF%9E%E6%8E%A52.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%86%85%E8%BF%9E%E6%8E%A53.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%86%85%E8%BF%9E%E6%8E%A54.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%86%85%E8%BF%9E%E6%8E%A56.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%86%85%E8%BF%9E%E6%8E%A57.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%86%85%E8%BF%9E%E6%8E%A58.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/sql%E4%B8%89%E9%83%A8%E6%B3%95.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%86%85%E8%BF%9E%E6%8E%A510.png)

## 左连接

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%B7%A6%E8%BF%9E%E6%8E%A51.png)

## 右连接

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%8F%B3%E8%BF%9E%E6%8E%A5.png)

## 多表联合查询,同名字段的处理方式

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%A4%9A%E8%A1%A8%E6%9F%A5%E8%AF%A2.png)

## 自关联

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%87%AA%E5%85%B3%E8%81%94.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%87%AA%E5%85%B3%E8%81%942.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%87%AA%E5%85%B3%E8%81%943.png)

## 子查询

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AD%90%E6%9F%A5%E8%AF%A21.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AD%90%E6%9F%A5%E8%AF%A22.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AD%90%E6%9F%A5%E8%AF%A23.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AD%90%E6%9F%A5%E8%AF%A24.png)

## concat拼接字符串函数

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/concat.png)

## length返回字符串字符的个数

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/length.png)

## mysql内置函数可以在where条件后面使用

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%86%85%E7%BD%AE%E5%87%BD%E6%95%B0.png)

## left从字符串左侧截取指定数量字符

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/left.png)

## right从字符串右侧截取指定数量的字符

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/right.png)

## substring从字符串指定位置截取指定数量字符

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/substring.png)

## 内置函数可以用在select显示的字段名中

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%86%85%E7%BD%AE%E5%87%BD%E6%95%B02.png)

## 课后练习

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%BE%E5%90%8E.png)

## ltrim去除字符串左侧空格

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/ltrim.png)

## rtrim去除字符串右侧空格

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/rtrim.png)

## trim去除字符串两个空格

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/trim.png)

## round四舍五入

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/round.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/round2.png)

## rand随机数

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/rand.png)

## 时间

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%97%B6%E9%97%B4.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%97%B6%E9%97%B4%E6%A1%88%E4%BE%8B.png)

## 存储过程

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%AD%98%E5%82%A8%E8%BF%87%E7%A8%8B.png)

## 视图

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%A7%86%E5%9B%BE.png)

## 事务

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E4%BA%8B%E5%8A%A11.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E4%BA%8B%E5%8A%A12.png)

![](D:\黑马测试学习路线\5.mysql\事务3.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E4%BA%8B%E5%8A%A14.png)

## 索引

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%B4%A2%E5%BC%951.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%B4%A2%E5%BC%952.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%B4%A2%E5%BC%953.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%B4%A2%E5%BC%954.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%B4%A2%E5%BC%955.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%B4%A2%E5%BC%956.png)

## Windows cmd命令窗口连接mysql

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/mysql1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/mysql2.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/mysql3.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/mysql4.png)

授权grant,回收revoke

