---
title: Linux介绍
date: '2022-8-3 17:58:00'
description: '目标:内含Linux操作系统介绍,Linux常用命令,vim编辑器'
cover: 'https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/17(1).webp'
categories:
  - - 计算机基础
tags:
  - Linux
abbrlink: ddbe5190
---

# Linux

VMware加载Linux(Ubuntu)

目标:

1. 掌握Linux常用的命令

## 操作系统

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F.png)

## 操作系统的作用

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F%E7%9A%84%E4%BD%9C%E7%94%A81.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F%E4%BD%9C%E7%94%A82.png)

## 不同应用领域的主流操作系统

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E4%B8%BB%E6%B5%81.png)

## Linux由来

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%94%B1%E6%9D%A5.png)

## Linux发行版本

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%8F%91%E8%A1%8C%E7%89%88%E6%9C%AC.png)

## Linux的应用领域

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%BA%94%E7%94%A8%E9%A2%86%E5%9F%9F.png)

## Linux基本使用说明

学会了unix就学会了Linux

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E4%BD%BF%E7%94%A8.png)

是VMware全屏或退出全屏(ctrl+alt+回车)

Linux关机(方法一在设置里图形化关机,方法二使用命令 shutdown -h now)

## Linux图形界面下查看根目录内容

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%96%87%E4%BB%B6.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%A0%B9%E7%9B%AE%E5%BD%95.png)

## Linux主要目录

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%9B%AE%E5%BD%95.png)

## 常用Linux命令的基本使用

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%91%BD%E4%BB%A4%E7%9A%84%E5%9F%BA%E6%9C%AC%E4%BD%BF%E7%94%A8.png)

## Linux下的常用快捷方式

* 上下键"快速调出历史执行过的命令"
* tab健,自动补全

## Linux查看帮助

* 命令 --help

  简化版的帮助信息

* man 命令

  空格:下翻一页

  b:上翻一页

  q:退出

## pwd查看当前所在目录

pwd:作用是查看当前所在的目录

## ls查看目录内容

ls是英文单词list的简写,其功能为列出目录的内容

Linux所有的目录和文件名大小写敏感

以.开头的文件为隐藏文件或者目录

./代表当前目录

../代表上一级目录

ls [目录名]

​	ls后面没有目录名,代表显示当前目录内容

​	ls后面又目录名,代表显示指导目录内容

```linux
#显示当前目录内容
ls
ls ./
#显示当前目录的子目录内容
ls abc
ls ./abc
#显示根目录内容
ls /
#显示根目录下的bin目录内容
ls /bin
#显示上级目录内容
ls ..
```

ls的常用参数:

* -a:显示指定目录下所有子目录与文件,包括隐藏文件
* -l:以列表方式显示文件的详细信息
* -h:配合-l以人性化的方式显示文件大小

```Linux
#显示所有文件
ls -a
#显示详细信息
ls -l
#显示详细信息,文件大小用人性化方式显示
ls -hl
#侠士所有文件的详细信息
ls -al
```

ls -l返回结果说明:

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%BF%94%E5%9B%9E%E7%BB%93%E6%9E%9C.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AF%B4%E6%98%8E.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%96%87%E4%BB%B6%E5%AD%98%E5%8F%96.png)

第一位:-代表文件,d代表目录

第二位:开始是文件存取控制

​	一共9各位,每三位是一组,分别是三组:文件拥有者,文件所属组和其他用户

​	每三位又有rwx

​	r:可读,w:可写,x:可执行

用户和组的概念:

每个目录或者文件一定会属于一个用户和一个组

用户名和组名可以相同

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/ls%E9%85%8D%E5%90%88%E9%80%9A%E9%85%8D%E7%AC%A6.png)

* *代表任意多个字符

```Linux
#查看以a结尾的文件,或者目录的内容
ls *a
#查看以a开头的文件或者目录的内容
ls a*
#只要名字中有a就显示
ls *a*
```

* ?代表任意一个字符

```linux
#a开头,后面任意一个字符
ls a?
#开始有一个任意字符,后面以a结尾
ls ?a
#查看名字只有两个字符的
ls ??
```

* []代表范围

```linux
#a或者b或者c开头,后面任意
ls [a,b,c]*
#a到f任意的一个开头,后面任意
ls [a-f]*
#只要名字中有a到f中的任意一个字符即可
ls *[a-f]*
```

## chmod修改文件权限

* 修改文件读取权限
* u=user文件所属用户
* g=group文件所属的组
* o=other其他用户
* a=all所有用户
* +赋权
* -去权
* =后面有的就会赋权,没有的就去权

```Linux
#给文件所有者给予可读权
chmod u+r a.txt
#给文件所有者去掉可读权
chmod u-r a.txt
#所有用户添加所有权限
chmod a+rwx a.txt
#只保留r,wx去掉
chmod o=r a.txt
```

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/3%E6%95%B0%E5%AD%97%E6%B3%95.png)

```linux
#所有用户所有权限
chmod 777 a.txt
#所有用户只保留x权限
chmod 111 a.txt
```

## cd切换目录

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%87%E6%8D%A2%E7%9B%AE%E5%BD%95.png)

cd - 回到切换之前的目录

绝对路径和相对路径:

* 绝对路径:在Linux下从根目录开始,在windows上从某一个盘符开始
* 相对路径:从当前目录开始

```linux
#进入当前目录下的子目录
cd abc
#进入跟根目录下的abc目录
cd /abc
#回到用户的主目录
cd
#返回上级目录的上级目录
cd ../..
#回到切换之前的目录
cd -
```

## touch创建文件

* 作用是创建文件或修改文件时间
* 注意
  1. 如果文件不存在,可以创建一个空白文件
  2. 如果文件已经存在,可以修改文件的末次修改日期

```linux
touch b.txt
```

## mkdir创建目录

* 通过mkdir命令可以创建新目录
* 注意:新建目录的名称,不能与当前目录中已有的目录或者文件同名
* mkdir 目录名
* mkdir -p 目录/目录   创建有嵌套关系的多级目录

```linux
#创建一个目录aaa
mkdir aaa
#创建一个有嵌套关系的多级目录a/b/c
mkdir -p a/b/c
```

## rm删除文件或目录

* 可通过rm删除文件或目录
* 注意:使用rm命令要小心,因为文件删除后不能恢复
* rm 文件
* rm -r 目录
* 当文件或者目录不存在的时候,rm会报错

-f:强制删除,忽略不存在的文件,无需提示

-r:删除目录时必须加此参数

```linux
#删除abc目录,即使abc目录不存在,也不报错
rm -rf abc
```

## cp复制文件

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%A4%8D%E5%88%B6%E6%96%87%E4%BB%B6.png)

```Linux
#把当前目录下的a.txt拷贝到abc目录下
cp a.txt abc/a.txt
#把abc目录下的a.txt拷贝到当前目录下
cp abc/a.txt a.txt 
```

## mv移动文件

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%A7%BB%E5%8A%A8%E6%96%87%E4%BB%B6.png)

## cat查看文件内容

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/cat.png)

```Linux
#查看a.txt内容
cat a.txt
#/proc目录下面放了一些和系统信息相关文件
cd /proc
#查看Linux版本
cat version
#查看cpu信息
cat cpuinfo
```

## more分屏查看

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/more.png)

* 按空格向下翻一页
* b回看一页
* q退出

## grep在指定文件中查找指定的字符串

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/grep.png)

## echo回显

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/echo.png)

## clear清屏

清除屏幕显示历史内容

类似于dos下的cls

## 输出重定向

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%BE%93%E5%87%BA%E9%87%8D%E5%AE%9A%E5%90%91.png)

## 管道符号

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%AE%A1%E9%81%93.png)

```linux
#把ls -al的结果作为more的输入,结果就是可以间接的实现ls的分屏显示
ls -al | more
#ls -al结果只显示目录
ls -al | grep "^d"
#ls -al只显示名字以s结尾的目录
ls -al | grep "^d.*s$"
```

## cat结合重定向实现合并文件内容

cat a.txt b.txt > c.txt

把a.txt和b.txt 文件里的内容合并到c.txt里边

## find查找指定文件

find 开始目录 -name 文件名

```linux
#从当前目录开始查找所有子目录,是否存在a.txt文件
find ./ -name a.txt
#从根目录开始查找所有子目录,是否存在a.txt文件
find / -name a.txt
```

注意:

如果省略路径,默认是当前目录

## ln创建链接文件

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/ln.png)

硬链接文件,用ls -l显示文件硬链接数会增加

## Linux权限的含义

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%9D%83%E9%99%90.png)

# vi编辑器

## gzip压缩与解压

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/gzip1.png)

```
gzip a.txt
#把a.txt压缩为a.txt.gz,同时a.txt文件不存在了
gzip -d a.txt.gz
#把a.txt.gz解压,解压之后生成a.txt,a.txt.gz就不存在了
```

## zip压缩和解压文件

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/zip1.png)

```Linux
zip a.zip a.txt
#把a.txt压缩为a.zip,压缩完成之后a.txt还存在
unzip a.zip
#把a.zip解压,解压完成之后,a.zip还存在
```

## tar打包与解包

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/tar.png)

```linux
#把abc目录打包为一个文件abc.tar
tar -cvf abc.tar abc
#查看abc.tar文件的内容
tar -tvf abc.tar
#将abc.tar还原
tar -xvf abc.tar
```

## tar与gzip

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/tar%E4%B8%8Egzip.png)

```Linux
#把abc打包之后同时用gzip压缩
tar -zcvf abc.tar.gz abc
#把bc.tar.gz用gzip解压之后用tar解包
tar -zxvf abc.tar.gz
```

## df磁盘剩余

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/df.png)

## ps查看进程

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/ps1.png)

一般情况下,把三者都加上使用

ps -aux 或者ps aux:显示系统中所有的进程,并且显示进程的详细信息

## top显示进程运行状态

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/top1.png)

## kill杀死进程

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/kill.png)

```linux
kill PID
kill -9 PID 当用kill PID杀不掉,那么就用-9参数,强行杀死
#在图形界面下,启动了gedit程序,用kill杀掉
ps aux | grep 'gedit'
kill gedit的PID
```

## ping检查网络是否连通

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/ping1.png)

Linux还一直ping,结束用ctrl+c结束

ping用ipv4的地址

## ifconfig查看网卡信息

* ifconfig

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/ifconfig.png)

## root用户

root用户权限很高,我们一般都是普通用户

## su切换用户

su - 用户名

需要输入密码(注意,在Linux输入密码的时候不回显)

退回su之前的用户:exit

su - 用户名与 su 用户名

* su - 用户名表示切换用户,同时改变了当前目录为用户的主目录
* su 用户名表示切换用户,但不改变当前目录

如果要切换的是root,su后面可以省略用户名root

* su - 等同于 su - root
* su 等同于 su root

其他用户切换root用户需要输入密码,root切换到其他用户不需要密码

su完之后一定要用exit退出,而不要不停的su到新用户

## useradd新增用户

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/useradd.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/useradd1.png)

## passwd改密码

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/passwd.png)

## userdel删除用户

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/userdel.png)

## whoami查看当前登录用户名

whoami

## vi编辑器三种模式介绍

![](D:\黑马测试学习路线\4.Linux(内含Linux操作系统介绍,Linux常用命令,vim编辑器)\vi1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/vi22.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/vi3.png)

## vi的三种启动方式

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/vi%E5%90%AF%E5%8A%A8.png)

## vi的三种退出方式

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/vi%E9%80%80%E5%87%BA.png)

## vi案例-修改配置文件

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/vi%E7%BC%96%E8%BE%91.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/vi%E7%BC%96%E8%BE%912.png)

## vi命令模式下的常用命令

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%B8%B8%E7%94%A8%E5%91%BD%E4%BB%A411.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%B8%B8%E7%94%A8%E5%91%BD%E4%BB%A433.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%B8%B8%E7%94%A8%E5%91%BD%E4%BB%A422.png)

## 末行模式

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%9C%AB%E8%A1%8C.png)











