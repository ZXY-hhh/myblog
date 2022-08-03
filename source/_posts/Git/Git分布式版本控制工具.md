---
title: Git分布式版本控制工具
date: '2022-8-3 10:58:00'
description: '目标:1.了解Git基本概念;2.能够概述Git工作流程;3.能够使用Git常用命令;4.熟悉Git代码托管服务;5.能够使用idea操作Git'
sticky: 1
cover: 'https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/6(1).webp'
abbrlink: e01dd7d7
categories: 
 - [Git]
 - [版本控制]
tags:
 - Git基本概念
 - Git工作流程
 - Git代码托管
 - 使用idea操作Git

---

# Git分布式版本控制工具

## 1、目标

* 了解Git基本概念
* 能够概述Git工作流程
* 能够使用Git常用命令
* 熟悉Git代码托管服务
* 能够使用idea操作Git

## 2、概述

### 2.1、开发中的实际场景

```选择语言
场景一:备份
	小明负责的模块就要完成了,就在即将release之前的一瞬间,电脑突然蓝屏,硬盘光荣牺牲!几个月来的努力付之东流.
场景二:代码还原
	这个项目需要一个很复杂的功能,老王摸索了一个星期终于有了眉目,可是这被改得面目全非的代码已经回不来到从前了.什么地方能买到哆啦A梦的时光机啊?
场景三:协同开发
	小刚和小强先后从文件服务器上下载了同一个文件:Analysis.java,小刚在Analysis.java文件中的第30行声明了一个方法,叫count(),先保存到了文件服务器上;小强在Analysis.Java文件中的第50行声明了一个方法,叫sum(),也随后保存到了文件服务器上,于是,count()方法就只存在于小刚的记忆中了
场景四:追溯问题代码的编写人和编写时间
	老王是另一位项目经理,每次因为项目进度挨骂之后,他都不知道该扣那个程序员的工资!就拿这次来说吧,有个Bug调试了30多个小时才知道是因为相关属性没有在应用初始化时赋值!可是二胖,王东,刘流和正经牛都不承认是自己干的!
```

### 2.2、版本控制的方式

```选择语言
1.集中式版本控制工具
	集中式版本控制工具,版本库是集中存放在中央服务器的,team里每个人work时从服务器下载代码,是必须联网才能工作,局域网或互联网.个人修改然后提交到中央版本库.
	举例:SVN和CVS
2.分布式版本控制工具
	分布式版本控制系统没有"中央服务器",每个人的电脑上都是一个完整的版本库,这样工作的时候,无需要联网了,因为版本库就在自己的电脑上.多人协作只需要各自修改推送给对方,就能互相看到对方的修改了.
	举例:Git
```

### 2.3、SVN

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/svn.png)

### 2.4、Git

```选择语言
	git是分布式的,git不需要有中心服务器,我们每台电脑拥有的东西都是一样的.我们使用git并且有个中心服务器,仅仅是为了方便交换大家 的修改,但是这个服务器的地位和我们每个人夫人pc是一样的.我们可把他当作一个开发者的pc就可以,就是为了大家代码容易交流不关机用的.没有它大家一样可以工作,只不过"交换"修改不方便而已.
	git是一个开源的分布式版本控制工具,可以是有效,高速地处理从很小到非常大的项目版本管理.git是Linus Torvalds 为了帮助管理 Linux内核开发而开发的一个开放源码的版本控制软件.
	同生活中的许多伟大的事物一样,git诞生于一个极富纷争大举创新的年代.Linux内核开源项目有着为数众多的参与者.绝大多数的Linux内核维护工作都花在了提交补丁和保存归档的繁琐事务上(1991-2002年间).到2002年,整个项目组开始启用一个专有的分布式版本控制系统BitKeeper来管理和维护代码.
	到了2005年,开发BitKeeper的商业公司同Linux内核开源社区的合作关系结束,他们收回了Linux内核社区免费使用BitKeeper的权利.这就迫使Linux开源社区(也别是Linux的缔造者Linus Torvalds)基于使用BitKeeper时的经验教训,开发出自己的版本系统.她们对新的系统制定了若干目标:
	速度
	简单的设计
	对非线性开发模式的强大支持(允许成千上万个并行开发的分支)
	完全分布式
	有能力高效管理类似Linux内核一样的超大规模项目(速度和数据量)
```

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/git.png)

### 2.5、Git工作流程图

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%B7%A5%E4%BD%9C%E6%B5%81%E7%A8%8B%E5%9B%BE.png)

命令如下:

1. clone(克隆):从远程仓库中克隆代码到本地仓库
2. checkout(检出):从本地仓库中检出一个仓库分支然后进行修订
3. add(添加):在提交前先将代码提交到暂存区
4. commit(提交):提交到本地仓库.本地仓库中保存修改的各个历史版本
5. fetch(抓取):从远程库,抓取到本地仓库,不进行任何的合并动作,一般操作比较少.
6. pull(拉取):从远程库拉到本地库,自动进行合并(merge),然后放到工作区,相当于fetch+merge
7. push(推送):修改完成后,需要和团队成员共享代码时,将代码推送到远程仓库

## 3、Git安装与常用命令

本教程里的git命令例子都是在Git Bash中演示的,会用到一些基本的Linux命令,在此为大家提前列举:

* ls/ll	查看当前目录
* cat    查看文件内容
* touch 创建文件
* vi     vi编辑器(使用vi编辑器是为了方便展示效果,学员可以记事本,editPlus,notPad++等其他编辑器)

### 3.1、Git环境配置

#### 3.1.1 下载与安装

下载地址:https://git-scm.com/download

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/dowanload.png)

下载完成后可以得到如下安装文件:

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/exe.png)

双击下载的安装文件来安装git,安装完成后在电脑桌面(也可以是其他目录)点击右键,如果能够看到如下两个菜单则说明git安装成功.

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%88%90%E5%8A%9F.png)

备注:

​	Git GUI:Git提供的图形界面工具

​	Git Bash:Git提供的命令行工具

​	当安装Git后首先要做的事情是设置用户名称和email地址.这是非常重要的,因为每次Git提交都会使用该用户信息

#### 3.1.2 基本配置

1. 打开Git Bash

2. 设置用户信息

   git config --global user.name "itcast"

   git config --global user.email "hello@itcast.cn"

3. 查看配置信息

   git config --global user.name

   git config --global user.email

#### 3.1.3为常用指令配置别名(可选)

有些常用的指令参数非常多,每次都要输入好多参数,我们可以使用别名.

1. 打开用户目录,创建.bashrc文件

   部分windows系统不允许用户创建点号开头的文件,可以打开gitBash,执行 touch ~/.bashrc

   ~表示当前目录的根目录

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/bashrc.png)

2. 在.bashrc文件中输入如下内容:

   ```shell
   #用于输出git提交日志
   alias git-log='git log --pretty=oneline --all --graph --abbrev-commit'
   #用于输出当前目录所有文件及基本信息
   alias ll='ls -al'
   ```

3. 打开gitBash,执行source ~/.bashrc

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/souce.png)

#### 3.1.4 解决GitBash乱码问题

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E4%B9%B1%E7%A0%81%E8%AE%BE%E7%BD%AE.png)

### 3.2、获取本地仓库

要使用Git对我们的代码进行版本控制,首先需要获得本地仓库

(1)在电脑的任意位置创建一个空目录(例如test)作为我们的本地Git仓库

(2)进入这个目录中,点击右键打开Git bash窗口

(3)执行命令git init

(4)如果创建成功后可在文件夹下看到隐藏的.git目录

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%8E%B7%E5%8F%96%E6%9C%AC%E5%9C%B0%E4%BB%93%E5%BA%93.png)

### 3.3、基础操作指令

Git工作目录(除了.git文件外的目录叫做工作目录)下对于文件的修改(增加,删除,更新)会存在几个状态,这些修改的状态会随着我们执行Git命令而发生变化.

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%9F%BA%E7%A1%80%E6%93%8D%E4%BD%9C%E6%8C%87%E4%BB%A4.png)

本章节主要讲解如何使用命令来控制状态之间的转换:

1. git add (工作区-->暂存区)
2. git commit (暂存区-->本地仓库)

#### 3.3.1、查看修改的状态(status)

* 作用:查看的修改的状态(暂存区、工作区)
* 命令形式:git status

#### 3.3.2、添加工作区到暂存区(add)

* 作用:添加工作区一个或多个文件的修改到暂存区

* 命令形式:git add 单个文件名|通配符

  将所有修改加入暂存区:git add .(.表示所有)

#### 3.3.3、提交暂存区到本地仓库(commit)

* 作用:提交暂存区内容到本地仓库的当前分支
* 命令形式:git commit -m '注释内容'

#### 3.3.4、查看提交日志(log)

在3.1.3中配置的别名git-log就包含了这些参数,所以后续可以直接使用指令git-log

* 作用:查看提交记录

* 命令形式:git log [option]

  options

  ​	--all 显示所有分支

  ​	--pretty=oneline 将提交信息显示为一行

  ​	--abbrev-commit 使得输出得commitld更简短

  ​	--graph 以图得形式显示

#### 3.3.5、版本回退

* 作用:版本切换

* 命令形式:git reset --hard commitID

  commitID可以使用git-log或git log指令查看

* 如何查看已经删除得记录?

  git reflog(把所有的版本操作都记录下来了)

  这个指令可以看到已经删除的提交记录

  注意:

  这里选中即表示已经复制(不需要用CTRL C因为它在Linux中有其他的设置)

  选中之后即表示已经复制好,那么粘贴也不要使用ctrl+v,直接按一下滚轮,或者使用右键,选中粘贴也行.

  ![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%89%88%E6%9C%AC%E5%9B%9E%E9%80%80.png)

#### 3.3.6、添加文件至忽略列表

一般我们总会有些文件无需纳入git的管理,也不希望它们总出现在未跟踪文件列表.通常都是些自动生成的文件,比如日志文件,或者编译过程中创建的临时文件等.在这种情况下,我们可以在工作目录中创建一个名为.gitignore的文件(文件名称固定),列出要忽略的文件模式.下面是一个示例:

在.gitignore文件中写上不需要git管理的文件,表示不需要管理所有的.a的文件.

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%AE%A1%E7%90%86%E6%96%87%E4%BB%B6.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%A4%BA%E4%BE%8B.png)

实际操作:

首先从这个工作目录下打开git bash

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/2.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/3.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/4.png)

这里git add有两种方法:(1)git add 文件名;(2)git add' .表示所有add(这里习惯用这种)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/5.png)

修改文件

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/6.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/7.png)

### 3.4、分支

几乎所有的版本控制系统都以某种形式支持分支.使用分支意味着你可以把你的工作从开发主线上分离开来进行重大的bug修改,开发新的功能,以免影响开发主线.

#### 3.4.1、查看本地分支

* 命令:git branch

#### 3.4.2、创建本地分支

* 命令:git branch 分支名

#### 3.4.3、切换分支(checkout)

* 命令:git checkout 分支名

  我们还可以直接切换到一个不存在的分支(创建并切换)

* 命令:git checkout -b 分支名

#### 3.4.4、合并分支(merge)

一个分支上的提交可以合并到另一个分支

命令:git merge 分支名称

合并的快进模式:

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%90%88%E5%B9%B6%E7%9A%84%E5%BF%AB%E8%BF%9B%E6%A8%A1%E5%BC%8F.png)

#### 3.4.5、删除分支

不能删除当前分支,只能删除其他分支

git branch -d b1 删除分支时,需要做各种检查

git branch -D b1 不做任何检查,强制删除

#### 3.4.6、解决冲突

当两个分支上对文件的修改可能会存在冲突,例如同时修改了同一个文件的同一行,这时就需要手动解决冲突,解决冲突步骤如下:

1. 处理文件中冲突的地方
2. 将解决完冲突的文件加入暂存区(add)
3. 提交到仓库(commit)

冲突部分的内容处理如下所示:

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%86%B2%E7%AA%81.png)

#### 3.4.7、开发中分支使用原则与流程

几乎所有的版本控制系统都是以某种形式支持分支.使用分支意味着你可以把你的工作从开发主线上分离开来进行重大的bug修改,开发新的功能,以免影响开发主线.

在开发中,一般有如下分支使用原则与流程:

* master(生产)分支

  线上分支,主分支,中小规模项目作为线上运行的应用对应的分支;

* develop(开发)分支

  是从master创建的分支,一般作为开发部门的主要开发分支,如果没有其他并行开发不同期上线要求,都可以在此版本进行开发,阶段开发完成后,需要是合并到master分支,准备上线.

* feature/xxxx分支

  从develop创建的分支.一般是同期并发开发,但不同期上线时创建的分支,分支上的研发任务完成后合并到develop分支.

* hotfix/xxxx分支

  从master派生的分支,一般作为线上bug修复使用,修复完成后需要合并到master,test,develop分支.

* 还有一些其他分支,在此不再详述,例如test分支(用于代码测试),pre分支(预上线分支)等等.

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%BC%80%E5%8F%91%E4%B8%AD%E5%88%86%E6%94%AF%E7%9A%84%E5%8E%9F%E5%88%99.png)

## 4、Git远程仓库

### 4.1、常用的托管服务[远程仓库]

```选择语言
前面我们已经知道了Git中存在两种类型的仓库,即本地仓库和远程仓库.那么我么如何搭建Git远程仓库呢?我们可以借助互联网上提供的一些代码托管来实现,其中比较常见的有GitHub,码云,GitLab等.
GitHub(地址:https://github.com/)是一个面向开源及私有软件项目的托管平台,因为只支持git作为唯一的版本库格式进行托管,故名GitHub
码云(地址:https://gitee.com/)是国内的一个代码托管平台,由于服务器在国内,所以相比于GitHub,码云速度会更快.
gitlab(地址:https://about.gitlab.com/)是一个用于仓库管理系统的开源项目,使用git作为代码管理工具,并在此基础上搭建起来的web服务,一般用于企业,学校等内部网络搭建git私服.
```

### 4.2、注册码云

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%B3%A8%E5%86%8C%E7%A0%81%E4%BA%91.png)

### 4.3、创建远程仓库

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%9B%E5%BB%BA%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%931.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%9B%E5%BB%BA%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%932.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%9B%E5%BB%BA%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%933.png)

### 4.4、配置SSH公钥

* 生成SSH公钥

  ssh-keygen-t rsa

  不断回车

  ​	如果公钥已经存在,则自动覆盖

* Gitee设置账户共公钥

  获取公钥

  ​	cat ~/.ssh/id_rsa.pub

  ![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%85%AC%E9%92%A5.png)

* 验证是否配成功

  ssh-T git@gitee.com

后面回答yes即可

### 4.5、操作远程仓库

#### 4.5.1、添加远程仓库

此操作是先初始化本地库,然后与已创建的远程库进行对接

* 命令:git remote add <远端名称> <仓库路径>

  远端名称,默认是origin,取决于远端服务器设置

  仓库路径,从远端服务器获取此url

  例如:git remote add origin git@gitee.com:czbk_zhang_meng/git_test.git

  ![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%B7%BB%E5%8A%A0%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93.png)

#### 4.5.2、查看远程仓库

* 命令:git remote

  ![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%9F%A5%E7%9C%8B%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93.png)

####  4.5.3、推送到远程仓库

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8E%A8%E9%80%81%E5%88%B0%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93.png)

* 命令:git push [-f] [--set-upstream] [远端名称[本地分支名] [:远端分支名]]

  如果远程分支名和本地分支名称相同,则可以只写本地分支

  git push origin master

  -f表示强制覆盖

  --set-upstream推送到远端的同时并且建立起和远端分支的关联关系

  git push --set-upstream origin master

  如果当前分支已经和远端分支关联,则可以省略分支名和远端名

  git push将master分支推送到已关联的远端分支.

  ![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8E%A8%E9%80%812.png)

验证是否推上去

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%9F%A5%E8%AF%A2%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93.png)

#### 4.5.4、本地分支与远程分支的关联关系

* 查看关联关系我们可以使用git branch -vv命令

  ![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%9F%A5%E7%9C%8B%E5%85%B3%E8%81%94%E5%85%B3%E7%B3%BB.png)

#### 4.5.5、从远程仓库克隆

如果已经有一个远端仓库,我们可以直接clone到本地

* 命令:git clone <仓库名称> [本地目录]

  ![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%85%8B%E9%9A%86.png)

本地目录可以省略,会自动生成一个目录(也就是以.git前面的git_test生成一个本地仓库的目录)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%85%8B%E9%9A%861.png)

对于同一个仓库,一般只克隆一次

#### 4.5.6、从远程仓库中抓取和拉取

远程分支和本地分支一样,我们可以进行merge操作,只是需要先把远程仓库里的更新都下载到本地,在进行操作.

* 抓取命令:git fetch [remote name] [branch name]

  抓取指令就是将仓库里的更新都抓取到本地,不会进行合并

  如果不指定远端名称和分支名,则抓取所有分支

* 拉取命令:git pull [remote name] [branch name]

  拉去指令就是将远端仓库的修改拉到本地并自动进行合并,等同于fetch+merge

  如果不指定远端名称和分支名,则抓取所有并更新当前分支.

  ![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8E%A8%E9%80%81.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8B%89%E5%8F%96.png)

注意:

退出vi编辑器要按esc,然后再输入:wq即退出了

#### 4.5.7、解决合并冲突

在一段时间,A,B用户修改了同一个文件,且修改了同一行位置的代码,此时会发生合并冲突.

A用户在本地修改代码后优先推送到远程仓库,此时B用户再本地修订代码,提交到本地仓库后,也需要推送到远程仓库,此时B用户晚于A用户,故需要先拉取远程仓库的提交,经过合并后才能推送到远端分支,如下图所示.

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%A7%A3%E5%86%B3%E5%90%88%E5%B9%B6%E5%86%B2%E7%AA%81.png)

再B用户拉取代码时,因为A,B用户同一段时间修改了同一个文件的相同位置的代码,故会发生合并冲突.

远程分支也是分支,所有合并冲突的解决方式也和解决本地冲突的方式相同.

练习:

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%BB%83%E4%B9%A01.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E7%BB%83%E4%B9%A02.png)

## 5、在Idea中使用Git

### 5.1、在Idea中配置Git

安装好Intellij IDEA后,如果Git安装在默认路径下,那么idea会自动找到git的位置,如果更改了Git的安装位置则需要手动配置Git的路劲,选择File->Settings打开设置窗口,找到Version Control下的git选项:
![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/idea.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/idea2.png)

### 5.2、在Idea中操作Git

场景:本地已经有一个项目,但是并不是git项目,我们需要将这个放到码云的仓库里,和其他开发人员继续一起协作开发.

#### 5.2.1、创建项目远程仓库

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%96%B0%E5%BB%BA%E4%BB%93%E5%BA%931.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%96%B0%E5%BB%BA%E4%BB%93%E5%BA%932.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%9B%E5%BB%BA1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%9B%E5%BB%BA2.png)

#### 5.2.2、初始化本地仓库

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%9D%E5%A7%8B%E5%8C%96%E6%9C%AC%E5%9C%B0%E4%BB%93%E5%BA%93.png)

#### 5.2.3、设置远程仓库

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AE%BE%E7%BD%AE%E8%BF%9C%E7%A8%8B%E4%BB%93%E5%BA%93.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AE%BE%E7%BD%AE1.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AE%BE%E7%BD%AE2.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%AE%BE%E7%BD%AE3.png)

#### 5.2.4、提交到本地仓库

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8F%90%E4%BA%A4%E5%88%B0%E6%9C%AC%E5%9C%B0%E4%BB%93%E5%BA%93.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8F%90%E4%BA%A41.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8F%90%E4%BA%A42.png)

#### 5.2.5、推送到远程仓库

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8F%90%E4%BA%A43.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E6%8F%90%E4%BA%A44.png)

在接下来的完成修改之后也是这样推送到远程仓库,只是和第一次有一些不一样

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E9%87%8D%E6%8E%A81.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E9%87%8D%E6%8E%A82.png)

#### 5.2.6、克隆远程仓库到本地

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%85%8B%E9%9A%8611.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%85%8B%E9%9A%8622.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%85%8B%E9%9A%8633.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%85%8B%E9%9A%8644.png)

当两个开发在同一文件的统一代码上进行修改时,当第一个完成的能够push上去,后面的这个人就需要先pull一下,merge之后才能推.

这里演示第二个人要怎么操作解决冲突

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%A7%A3%E5%86%B31.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%A7%A3%E5%86%B32.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%A7%A3%E5%86%B33.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%A7%A3%E5%86%B34.png)

解决好冲突代码之后要把红色报错部分改成蓝色,所以右击红色文件

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%A7%A3%E5%86%B35.png)

最后commit然后push上去

#### 5.2.7、创建分支

* 最常规的方式

  ![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%86%E6%94%AF1.png)

* 最强大的方式

  ![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%86%E6%94%AF2.png)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%86%E6%94%AF3.png)

#### 5.2.8、切换分支及其他分支相关的操作

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%88%86%E6%94%AF4.png)

#### 5.2.9、解决冲突

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E8%A7%A3%E5%86%B3%E5%86%B2%E7%AA%81.png)

### 5.3、IDEA常用GIT操作入口

1.第一张图上的快捷入口可以基于满足开发的需求

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/idea%E6%93%8D%E4%BD%9C.png)

2.第二张图是更多在IDEA操作git的入口

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/idea%E6%93%8D%E4%BD%9C1.png)

### 5.4、场景分析

基于我们后面的实战模拟,我们做一个综合练习

当前的开发环境如下,我们每个人都对这个项目已经开发一段时间,接下来我们要切换成团队开发模式.

也就是我们由一个团队来完成这个项目实战的内容.团队由组长和若干组员组成(组长就是开发中的项目经理).所有操作在idea中完成.

来呢西场景如下:

1.由组长,基于本项目创建本地仓库;创建远程仓库,推送项目到远程仓库.

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%9C%BA%E6%99%AF1.png)

2.每一位组员从远程仓库克隆项目到idea中,这样每位同学在自己的电脑上就有了一个工作副本,可以证实的开始开发了.我们模拟两个组员(组员A,组员B),克隆两个工作区.

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%9C%BA%E6%99%AF2.png)

3.组员A修改工作区,提交到本地仓库,再推送到远程仓库.组员B可以直接从远程仓库获取最新的代码.

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%9C%BA%E6%99%AF3.png)

4.组员A和组员B修改了同一个文件的同一行,提交到本地没有问题,但是推送到远程仓库时,后一个推送操作就会失败.

解决方法:需要先获取远程仓库的代码到本地仓库,编辑冲突,提交并推送代码.

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E5%9C%BA%E6%99%AF4.png)

## 附:几条铁令

1.切换分支前先提交本地的修改

2.代码及时提交,提交过了就不会丢

3.遇到任何问题都不要删除文件目录

## 附:疑难问题解决

1.windows下看不到隐藏文件(.bashrc)

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E9%9A%90%E8%97%8F%E6%96%87%E4%BB%B6.png)

## 附:IDEA集成GitBash作为Terminal

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/terminal.png)

## git常用指令速查

![](https://cdn.jsdelivr.net/gh/ZXY-hhh/picgo/img/%E9%80%9F%E6%9F%A5png.png)







