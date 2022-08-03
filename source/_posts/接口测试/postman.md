---
title: postman接口测试
date: '2022-8-3 10:58:00'
description: >-
  目标: 1. 基础应用:接口测试简介,接口测试流程,接口测试用例设计,实战接口介绍 2. 基础应用:postman简介和安装以及postman的登录和注册
  3. 基础应用:postman接口请求实战以及界面页签详解 4. 基础应用:postman环境变量和全局变量 5. 基础应用:postman接口关联实战
  6. 进阶实战:postman内置动态参数以及自定义动态参数 7. 进阶实战:postman常规断言,动态参数断言以及全局断言 8.
  进阶实战:postman接口测试之CSV或json文件实现数据驱动 9. 进阶实战:postman必须带请求头的接口测试实战以及常用请求头详解 10.
  进阶实战:postman实现接口Mock Server自定义接口服务器 11. 进阶实战:postman接口测试(cookie鉴权以及token鉴权实战)
  12. 进阶实战:postman接口加密(base64.md5,rsa.des,res)解密实战 13.
  持续集成:postman+Newman+jenkins实现接口自动化测试持续集成
cover: 'https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/5(1).webp'
categories:
  - - 接口测试
  - - 接口自动化
  - - 自动化
tags:
  - postman
abbrlink: b9220a47
---

# postman

目标:

1. 基础应用:接口测试简介,接口测试流程,接口测试用例设计,实战接口介绍
2. 基础应用:postman简介和安装以及postman的登录和注册
3. 基础应用:postman接口请求实战以及界面页签详解
4. 基础应用:postman环境变量和全局变量
5. 基础应用:postman接口关联实战
6. 进阶实战:postman内置动态参数以及自定义动态参数
7. 进阶实战:postman常规断言,动态参数断言以及全局断言
8. 进阶实战:postman接口测试之CSV或json文件实现数据驱动
9. 进阶实战:postman必须带请求头的接口测试实战以及常用请求头详解
10. 进阶实战:postman实现接口Mock Server自定义接口服务器
11. 进阶实战:postman接口测试(cookie鉴权以及token鉴权实战)
12. 进阶实战:postman接口加密(base64.md5,rsa.des,res)解密实战
13. 持续集成:postman+Newman+jenkins实现接口自动化测试持续集成



![](D:\黑马测试学习路线\接口测试2\1.png)

![](D:\黑马测试学习路线\接口测试2\2.png)

![](D:\黑马测试学习路线\接口测试2\3.png)

![](D:\黑马测试学习路线\接口测试2\4.png)

![](D:\黑马测试学习路线\接口测试2\5.png)

![](D:\黑马测试学习路线\接口测试2\6.png)

![](D:\黑马测试学习路线\接口测试2\7.png)

![](D:\黑马测试学习路线\接口测试2\8.png)

![](D:\黑马测试学习路线\接口测试2\9.png)

![](D:\黑马测试学习路线\接口测试2\10.png)

![](D:\黑马测试学习路线\接口测试2\11.png)

```
// console.log(responseBody);
// 使用json提取器提取access_token值
// 把返回的字符串格式的数据转换成对象的形式
var result = JSON.parse(responseBody);
console.log(result.access_token)
// 把access_token设置为全局变量
pm.globals.set("access_token", result.access_token);
```

```
//使用正则表达式提取器实现接口关联,match匹配
var result = responseBody.match(new RegExp('"access_token":"(.*?)"'));
console.log(result[1]);
//设置为全局变量
pm.globals.set("access_token", result[1]);
```

![](D:\黑马测试学习路线\接口测试2\12.png)

![](D:\黑马测试学习路线\接口测试2\13.png)

![](D:\黑马测试学习路线\接口测试2\14.png)

![](D:\黑马测试学习路线\接口测试2\15.png)

![](D:\黑马测试学习路线\接口测试2\16.png)

![](D:\黑马测试学习路线\接口测试2\17.png)

![](D:\黑马测试学习路线\接口测试2\18.png)

![](D:\黑马测试学习路线\接口测试2\19.png)

![](D:\黑马测试学习路线\接口测试2\20.png)

![](D:\黑马测试学习路线\接口测试2\21.png)

![](D:\黑马测试学习路线\接口测试2\22.png)

![](D:\黑马测试学习路线\接口测试2\23.png)

![](D:\黑马测试学习路线\接口测试2\24.png)

接口加密解密

![](D:\黑马测试学习路线\接口测试2\25.png)

![](D:\黑马测试学习路线\接口测试2\26.png)

![](D:\黑马测试学习路线\接口测试2\27.png)

![](D:\黑马测试学习路线\接口测试2\28.png)

![](D:\黑马测试学习路线\接口测试2\29.png)

![](D:\黑马测试学习路线\接口测试2\30.png)

![](D:\黑马测试学习路线\接口测试2\31.png)

![](D:\黑马测试学习路线\接口测试2\32.png)

![](D:\黑马测试学习路线\接口测试2\33.png)

![](D:\黑马测试学习路线\接口测试2\34.png)

![](D:\黑马测试学习路线\接口测试2\35.png)

![](D:\黑马测试学习路线\接口测试2\36.png)

项目流程:

![](D:\黑马测试学习路线\接口测试2\37.png)

项目讲细节

![](D:\黑马测试学习路线\接口测试2\38.png)

![](D:\黑马测试学习路线\接口测试2\39.png)

mysql的多表查询,批量什么.....写多一点,细化一点

appid(ID):wx6b11b3efd1cdc290

secret(密钥):106a9c6157c4db5f6029918738f9529d

| 1.获取接口统一鉴权码token接口 |                                                              |        |                                                          |                                    |
| ----------------------------- | ------------------------------------------------------------ | ------ | -------------------------------------------------------- | ---------------------------------- |
| 请求url                       | https://api.weixin.qq.com/cgi-bin/token?grant_type=client_credential&appid=APPID&secret=APPSECRET |        |                                                          |                                    |
| 请求方式                      | GET                                                          |        |                                                          |                                    |
| 输入参数说明                  | 参数名                                                       | 必选   | 类型                                                     | 说明                               |
|                               | grant_type                                                   | 是     | string                                                   | 填写client_credential              |
|                               | appid                                                        | 是     | string                                                   | 第三方用户唯一凭证,即appid         |
|                               | secret                                                       | 否     | string                                                   | 第三方用户唯一凭证密钥,即appsecret |
| 返回示例                      | {"access_token":"ACCESS_TOKEN","expires_in":7200}            |        |                                                          |                                    |
| 返回参数说明                  | access_token                                                 | string | 接口统一鉴权码                                           |                                    |
|                               | expires_in                                                   | int    | 统一鉴权码有效时间,单位为秒,每次获取后前面的鉴权码将失效 |                                    |
| 错误码说明                    |                                                              |        |                                                          |                                    |
|                               |                                                              |        |                                                          |                                    |

标签管理接口

| 1.创建标签接口 |                                                              |      |        |                                         |
| -------------- | ------------------------------------------------------------ | ---- | ------ | --------------------------------------- |
| 请求url        | https://api.weixin.qq.com/cgi-bin/tags/create?access_token=ACCESS_TOKEN |      |        |                                         |
| 请求方式       | POST                                                         |      |        |                                         |
| 输入参数示例   | {"tag":{"name":"广东"}}                                      |      |        |                                         |
| 输入参数说明   | 参数名                                                       | 必选 | 类型   | 说明                                    |
|                | access_token                                                 | 是   | string | 统一接口鉴权码                          |
|                | name                                                         | 是   | string | 标签名,标签名不能和已经存在的标签名重复 |
|                |                                                              |      |        |                                         |
| 返回示例       | {"tag":{"id":134,"name":"广东"}}                             |      |        |                                         |
| 返回参数说明   | id                                                           | int  | 标签id |                                         |
|                | name                                                         | int  | 标签名 |                                         |
| 错误码说明     |                                                              |      |        |                                         |
|                |                                                              |      |        |                                         |



| 2.获取公众号已创建的标签接口 |                                                              |      |        |                |
| ---------------------------- | ------------------------------------------------------------ | ---- | ------ | -------------- |
| 请求url                      | https://api.weixin.qq.com/cgi-bin/tags/get?access_token=ACCESS_TOKEN |      |        |                |
| 请求方式                     | GET                                                          |      |        |                |
| 请求参数说明                 | 参数名                                                       | 必选 | 类型   | 说明           |
|                              | access_token                                                 | 是   | string | 接口统一鉴权码 |



| 3.删除标签接口 |                                                              |      |        |                     |
| -------------- | ------------------------------------------------------------ | ---- | ------ | ------------------- |
| 请求url        | https://api.weixin.qq.com/cgi-bin/tags/delete?access_token=ACCESS_TOKEN |      |        |                     |
| 请求方式       | POST                                                         |      |        |                     |
| 输入参数示例   | {"tag":{"id":134}}                                           |      |        |                     |
| 请求参数说明   | 参数名                                                       | 必选 | 类型   | 说明                |
|                | access_token                                                 | 是   | string | 接口统一鉴权码      |
|                | id                                                           | 是   | int    | 标签的id,id不能重复 |

| 3.编辑标签接口 |                                                              |      |        |                     |
| -------------- | ------------------------------------------------------------ | ---- | ------ | ------------------- |
| 请求url        | https://api.weixin.qq.com/cgi-bin/tags/update?access_token=ACCESS_TOKEN |      |        |                     |
| 请求方式       | POST                                                         |      |        |                     |
| 输入参数示例   | {"tag":{"id":134,"name":"广东人"}}                           |      |        |                     |
| 请求参数说明   | 参数名                                                       | 必选 | 类型   | 说明                |
|                | access_token                                                 | 是   | string | 接口统一鉴权码      |
|                | id                                                           | 是   | int    | 标签的id,id不能重复 |

| 4.上床图片接口 |                                                              |      |        |                         |
| -------------- | ------------------------------------------------------------ | ---- | ------ | ----------------------- |
| 请求url        | https://api.weixin.qq.com/cgi-bin/media/uploadimg?access_token=ACCESS_TOKEN |      |        |                         |
| 请求方式       | POST                                                         |      |        |                         |
| 输入参数示例   |                                                              |      |        |                         |
| 请求参数说明   | 参数名                                                       | 必选 | 类型   | 说明                    |
|                | access_token                                                 | 是   | string | 接口统一鉴权码          |
|                | media                                                        | 是   | string | form-data中媒体文件标识 |

实现接口关联的两种方式

![](D:\黑马测试学习路线\接口测试2\40.png)

![](D:\黑马测试学习路线\接口测试2\41.png)



































































































































































































