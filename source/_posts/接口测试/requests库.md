---
title: 基于python结合requests库实现接口自动化
date: '2022-8-3 10:58:00'
description: >-
  目标: 1. requests是什么 2. get,post,put,delete请求 3. 接口中session,cookie,token应用 4.
  基于unittest框架集成接口自动化
cover: 'https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/16(1).webp'
categories:
  - - 接口测试
  - - 接口自动化
  - - 自动化
tags:
  - requests
abbrlink: 9bd5ba29
---

# 基于python结合requests库实现接口自动化

大纲:

1. requests是什么
2. get,post,put,delete请求
3. 接口中session,cookie,token应用
4. 基于unittest框架集成接口自动化

## 接口自动化测试

### 概念

接口测试:是对系统或组件之间的接口进行测试,主要是校验数据的交换,传递和控制管理过程,以及相互逻辑依赖关系.

自动化测试:是把以人为驱动的测试行为转化为机器执行的一种过程

接口自动化测试:是把程序或工具代替人工自动的完成对接口进行测试的一种过程.

### 实现方式

1. 通过接口测试工具来实现,比如:jmeter,postman
2. 通过编写代码来实现(python-requests)

### 接口测试工具的不足

1. 测试数据不好控制(无法直接读取或存储json格式)
2. 不方便测试加密接口
3. 扩展能力不足(复杂业务逻辑,复杂断言)

## 什么是requests库?

### requests库介绍

1. 使用python语言编写
2. 使用开源协议,基于urllib库做的二次封装
3. requests库中封装了响应接口测试方法

### requests库安装及验证

1. 安装:pip install requests

2. 验证:pip show requests  -->   显示相应的版本信息

3. 注意:

   安装时,电脑必须连接互联网

## requests常用的请求方法

常见的HTTP请求方式:GET,POST,PUT,DELETE,HEAD,OPTIONS

使用requests发送网络请求非常简单,只需要调用HTTP请求所对应的方法即可

### get方法

```python
"""
目标:get 请求方法演练
案例:http://www.baidu.com
请求:
1.请求方法get
相应:
2.响应对象.url # 获取请求url
3.响应对象.status_code # 获取响应状态码
4.响应对象.text # 以文本形式显示响应内容
"""
# 1.导包
import requests
# 2.调用get
url = "http://www.baidu.com"
result = requests.get(url)  # result为响应的对象
# 3.获取请求url地址
print("请求url:",result.url)
# 4.获取响应状态码
print("状态码:",result.status_code)
# 5.获取响应信息,文本形式
print("文本响应内容:",result.text)
# 我们可以从响应的对象中获取我们想要的响应信息
```

请求含参数

```python
"""
目标:get 请求方法带参数演练
案例:
1. http://www.baidu.com?id=1001
2. http://www.baidu.com?id=1001,1002
3. http://www.baidu.com?id=1001&kw=北京
请求:
1.请求方法get
相应:
2.响应对象.url # 获取请求url
3.响应对象.status_code # 获取响应状态码
4.响应对象.text # 以文本形式显示响应内容
"""
# 1.导包
import requests
# 2.调用get
# url = "http://www.baidu.com?id=1001"  不推荐
url = "http://www.baidu.com"
# 案例1 定义字典
# params = {"id":1001}
# 案例2
# params = {"id":[1001,1002]} 不推荐
# params = {"id":"1001,1002"}  %2c ASCI值为逗号
# 案例3
params = {"id":1001,"kw":"北京"}  #使用多个键值方式
result = requests.get(url,params=params)  # result为响应的对象
# 3.获取请求url地址
print("请求url:",result.url)
# 4.获取响应状态码
print("状态码:",result.status_code)
# 5.获取响应信息,文本形式
print("文本响应内容:",result.text)
```

![](D:\黑马测试学习路线\requests库\1.png)

![](D:\黑马测试学习路线\requests库\2.png)

![](D:\黑马测试学习路线\requests库\3.png)

![](D:\黑马测试学习路线\requests库\4.png)

![](D:\黑马测试学习路线\requests库\5.png)

![](D:\黑马测试学习路线\requests库\6.png)

![](D:\黑马测试学习路线\requests库\7.png)

![](D:\黑马测试学习路线\requests库\8.png)

![](D:\黑马测试学习路线\requests库\9.png)

![](D:\黑马测试学习路线\requests库\10.png)

![](D:\黑马测试学习路线\requests库\11.png)

![](D:\黑马测试学习路线\requests库\12.png)

![](D:\黑马测试学习路线\requests库\13.png)

![](D:\黑马测试学习路线\requests库\14.png)

![](D:\黑马测试学习路线\requests库\15.png)

![](D:\黑马测试学习路线\requests库\16.png)

![](D:\黑马测试学习路线\requests库\17.png)

![](D:\黑马测试学习路线\requests库\18.png)

![](D:\黑马测试学习路线\requests库\19.png)

![](D:\黑马测试学习路线\requests库\20.png)

![](D:\黑马测试学习路线\requests库\21.png)

![](D:\黑马测试学习路线\requests库\22.png)

![](D:\黑马测试学习路线\requests库\23.png)

![](D:\黑马测试学习路线\requests库\24.png)

![](D:\黑马测试学习路线\requests库\25.png)

![](D:\黑马测试学习路线\requests库\26.png)

![](D:\黑马测试学习路线\requests库\27.png)

![](D:\黑马测试学习路线\requests库\28.png)

![](D:\黑马测试学习路线\requests库\29.png)

![](D:\黑马测试学习路线\requests库\30.png)

![](D:\黑马测试学习路线\requests库\31.png)

![](D:\黑马测试学习路线\requests库\32.png)

![](D:\黑马测试学习路线\requests库\33.png)

![](D:\黑马测试学习路线\requests库\34.png)

![](D:\黑马测试学习路线\requests库\35.png)

![](D:\黑马测试学习路线\requests库\36.png)

![](D:\黑马测试学习路线\requests库\37.png)

![](D:\黑马测试学习路线\requests库\39.png)

![](D:\黑马测试学习路线\requests库\40.png)

![](D:\黑马测试学习路线\requests库\41.png)

![](D:\黑马测试学习路线\requests库\42.png)

![](D:\黑马测试学习路线\requests库\43.png)

![](D:\黑马测试学习路线\requests库\44.png)



































































































































































































































