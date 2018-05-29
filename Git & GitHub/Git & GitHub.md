# Git & GitHub
> By Kevin Song

[toc]
# 01 Git 简介
[Git 官方网站](https://git-scm.com/)
## 01-01 Git的诞生

世界各地大牛为开源的Linux写代码，庞大的代码需要管理

- 2002年以前：世界各地志愿者把代码通过diff方式发给Linus，Linus本人手工合并
    - 不使用CVS，SVN这些免费版本控制系统原因：
        - 集中式版本控制系统速度慢
        - 集中式版本控制系统必须联网
        - 其他商用版本控制系统需要付费，和Linux开源精神不符
- 2002年以后：Linux代码库太大，使用 BitMover公司免费授权的BitKeeper 进行版本控制
- 2005年：Linux大牛破解BitKeeper协议，BitKeeper公司收回免费使用权
- Linus用C自己写了一个分布式版本控制系统Git
- 2008年：GitHub网站上线，为开源项目免费提供Git存储

## 01-02 集中式vs分布式

### 集中式版本控制系统

**特点：** 版本库集中存放在中央服务器

工作流程：

- 从中央服务器取得最新版本
- Coding
- 向中央服务器上传修改后版本

缺点：

- 必须联网才能工作
- 如果网速慢，提交一个10M的文件要1个小时，血崩
- 安全性差，中央服务器挂了，所有人都干不了活

### 分布式版本控制系统

**特点：** 没有中央服务器

工作流程：

- 每个人电脑上都是一个完整的版本库
- Coding
- 互相推送修改后的版本

优点：

- 不需要联网就可以修改文件
- 安全性好，每个人电脑里都有完整的版本

### 其他收费版本控制系统

- ClearCase（IBM）：安装比WINDOWS大，速度血慢
- VSS（MicroSoft）：设计反人类，微软自己都不用

# 02 Git 安装

## 02-01 Linux
- 检验是否已经安装Git
```
$ git
The program 'git' is currently not installed. You can install it by typing:
sudo apt-get install git
```
- Debian或Ubuntu Linux下安装Git

```
sudo apt-get install git
```
## 02-02 Mac OS X

### 方法一

- 安装homebrew
- 通过homebrew安装Git
- 参考[homebrew文档](https://brew.sh/)

### 方法二

- 安装Xcode
- 菜单 - Xcode - Preferences - Downloads - Command Line Tools - Install

## 02-03 Windows

- 下载安装[Windows版Git](https://git-for-windows.github.io)
- Git - Git Bash 打开Git
- 设置名字和Email地址
```
$ git config --global user.name "Your Name"
$ git config --global user.email "email@example.com"
```

git config命令的--global参数：表示此机器上所有的Git仓库都会使用这个配置

# 03 Git 创建版本库

## 03-01 创建本地版本库

**1.** 创建空目录

```
$ mkdir learngit
$ cd learngit
$ pwd
/d/Git/learngit
```

pwd 命令用于显示当前目录

**2.** 通过 **git init** 把目录变成Git的repository

```
$ git init
Initialized empty Git repository in D：/Git/learngit/.git/
```

 **.git目录：**
 
 - 跟踪管理版本库
 - 不要手动修改
 - 默认是隐藏目录，用ls -ah 命令可以看见

## 03-02 添加文件到版本库

版本控制系统管理文件改动：

- 文本文件（txt文件，网页，程序代码）
    - 版本控制系统可以显示每次改动（第几行改了什么单词）
- 二进制文件（图片，视频）
    - 版本控制系统不能显示每次改动（只能知道文件大小改变了多少）

**1.** learngit目录下编写 readme.txt

```
Git is a version control system.
Git is free software.
```

**2.** git add 添加文件到 repository

```
$ git add readme.txt
```

什么也不显示就是添加好了：Unix哲学“没有消息就是好消息”

**3.** git commit 把文件提交到 repository

```
$ git commit -m "wrote a readme file"
[master (root-commit) 2f74cef] wrote a readme file
 1 file changed, 2 insertions(+)
 create mode 100644 readme.txt
```

git commit 命令详解

- **-m：** 输入本次提交说明，可以输入任意内容
- **x file changed：** x个文件被改动
- **x insertions(+)：** 插入了x行内容

可以add很多文件，一次性commit

## 03-03 删除本地版本库
本地版本库目录下打开Git Bash

```
$ rm -rf .git
```
# 04 Git 版本控制

**git status：** 查看仓库有没有被修改

```
$ git status
On branch master
nothing to commit, working directory clean
```
修改 readme.txt 后再次使用 git status
```
Git is a distributed version control system.
Git is free software.
```
```
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")
```
**git diff：** 查看文件修改了什么内容
```
$ git diff readme.txt
diff --git a/readme.txt b/readme.txt
index d8036c1..013b5bc 100644
--- a/readme.txt
+++ b/readme.txt
@@ -1,2 +1,2 @@
-Git is a version control system.
+Git is a distributed version control system.
 Git is free software.
\ No newline at end of file
```
确认提交

- git add
```
$ git add readme.txt
```
- git commit
```
$ git commit -m "add distributed"
[master e6d9050] add distributed
 1 file changed, 1 insertion(+), 1 deletion(-)
```

## 04-01 版本回退

修改readme.txt如下
```
Git is a distributed version control system.
Git is free software distributed under the GPL.
```
提交

```
$ git add readme.txt
$ git commit -m "append GPL"
[master a9d0c7a] append GPL
 1 file changed, 1 insertion(+), 1 deletion(-)
```
### 现在仓库有三个版本
版本1：wrote a readme file
```
Git is a version control system.
Git is free software.
```
版本2：add distributed
```
Git is a distributed version control system.
Git is free software.
```
版本3：append GPL
```
Git is a distributed version control system.
Git is free software distributed under the GPL.
```
**git log：** 查看版本

**git log --pretty=oneline：** 查看简单版本
```
$ git log
commit a9d0c7a4f503c94076a60980657d3198b55cdba3
Author: USERNAME <USERNAME@XX.com>
Date:   Thu Oct 12 18:30:17 2017 +0800

    append GPL

commit e6d9050da9cdb141c33b865946b38bf3e3a7ad56
Author: USERNAME <USERNAME@XX.com>
Date:   Thu Oct 12 18:27:04 2017 +0800

    add distributed

commit 2f74cef7a2afece8ce64b5f182850f216e109702
Author: USERNAME <USERNAME@XX.com>
Date:   Wed Oct 11 19:04:52 2017 +0800

    wrote a readme file
```
版本回退 **git reset**
```
$ git reset --hard HEAD^
HEAD is now at e6d9050 add distributed
```
版本前进 **git reset**
```
$ git reset --hard a9d0c7a4f
HEAD is now at a9d0c7a append GPL
```
- HEAD 当前版本
- HEAD^ 上一个版本
- HEAD^^ 上上个版本
- ...
- HEAD~100 上100个版本

如果忘记版本号无法前进，用 git reflog 查看所有操作

```
$ git reflog
a9d0c7a HEAD@{0}: reset: moving to a9d0c7a4f
e6d9050 HEAD@{1}: reset: moving to HEAD^
a9d0c7a HEAD@{2}: commit: append GPL
e6d9050 HEAD@{3}: commit: add distributed
2f74cef HEAD@{4}: commit (initial): wrote a readme file
```

## 04-02 工作区和暂存区
- 工作区（Working Directory）：learngit
- 版本库（Repository）：.git
    - 暂存区：stage
    - 分支：branch

**git add** 就是把文件从工作区移动到暂存区

**git commit** 就是把文件从暂存区提交到分支

### 示例
1. 修改 readme.txt 
```
Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
```
2. 新增一个 LICENSE 文件

git status 查看状态
```
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        LICENSE

no changes added to commit (use "git add" and/or "git commit -a")
```
3. 把两个文件add之后再次查看状态
```
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        new file:   LICENSE
        modified:   readme.txt
```
4. 提交到分支
```
$ git commit -m "understand how stage works"
[master b012805] understand how stage works
 2 files changed, 2 insertions(+), 1 deletion(-)
 create mode 100644 LICENSE
```
## 04-03 管理修改
Git 的优秀之处：跟踪并管理的是修改，而不是文件

1. 修改 readme.txt 
```
$ cat readme.txt
Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes.
```
2. 添加并查看状态

```
$ git add readme.txt

Administrator@2013-20150101XS MINGW64 /d/Git/learngit (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   readme.txt

```
3. 修改 readme.txt
```
$ cat readme.txt 
Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
```
4. 提交
```
$ git commit -m "git tracks changes"
[master 0792507] git tracks changes
 1 file changed, 2 insertions(+), 1 deletion(-)
```
5. 查看状态发现工作区并不是干净的
```
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

原因：第二次修改没有 add 到暂存区

第一次修改 -> git add -> 第二次修改 -> git commit

正解：第二次修改 add 到暂存区，commit合并两次修改一并提交

第一次修改 -> git add -> 第二次修改 -> git add -> git commit

**结论：** commit 之前一定要 add 到暂存区

## 04-04 撤销修改
- add 前撤销修改： git checkout
- add 后撤销修改：git reset HEAD file
- commit 后撤销修改：版本回退


### add 前撤销修改： git checkout

把文件在工作区的修改全部撤销

- add 前 修改 后 checkout（文件自修改后还没有被放到暂存区）
    - 撤销修改：回到和版本库一样的状态
    - （回到上次 git commit 的状态）
- add 后 修改 后  checkout（文件自修改后已经被被放到暂存区）
    - 撤销修改：回到添加到暂存区后的状态
    - （回到上次 git add 的状态）

1. 修改文件readme.txt
```
$ cat readme.txt
Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
My stupid boss still prefers SVN.
```
2. 撤销修改

```
$ git checkout -- readme.txt
```
3. 查看文件
```
$ cat readme.txt
Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
```


### add 后撤销修改：git reset HEAD file
1. 修改文件 readme.txt 并且 add 到暂存区
```
$ cat readme.txt
Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
My stupid boss still prefers SVN.

$ git add readme.txt
```
2. git reset HEAD file 把暂存区的修改撤销（unstage），重新放回工作区
```
$ git reset HEAD readme.txt
Unstaged changes after reset:
M       readme.txt
```
3. 丢弃工作区的修改
```
$ git checkout -- readme.txt

$ git status
# On branch master
nothing to commit (working directory clean)
```


## 04-05 删除文件
1. 先添加一个新文件test.txt到Git并且提交：

```
$ git add test.txt
$ git commit -m "add test.txt"
[master 94cdc44] add test.txt
 1 file changed, 1 insertion(+)
 create mode 100644 test.txt
```
2. 工作区删除文件
```
$ rm test.txt
```
3. 版本库删除文件
```
$ git rm test.txt
rm 'test.txt'
$ git commit -m "remove test.txt"
[master d17efd8] remove test.txt
 1 file changed, 1 deletion(-)
 delete mode 100644 test.txt
```
### 误删恢复
```
$ git checkout -- test.txt
```
git checkout 本质：用版本库里的版本替换工作区的版本

# 05 Git 远程仓库

**早期：**

- 一台电脑充当服务器，7 x 24 开机
- 别的机器可以克隆原始版本库

**现在：** GitHub（Git仓库托管服务）

本地Git仓库和GitHub仓库之间的传输是通过SSH加密：

1. 创建SSH Key
    - 用户主目录下有没有 **.ssh** 目录
        - **.ssh** 目录下有没有 **id_rsa** 和 **id_rsa.pub** 这两个密钥对。如果有直接去步骤 2
        - **id_rsa**：私钥
        - **id_rsa.pub** ：公钥
    - 用户主目录下没有 **.ssh** 目录
        - 打开 Git Bash 创建SSH Key
```
$ ssh-keygen -t rsa -C "youremail@example.com"
```

2. 登陆Github - Settings - SSH and GPG Keys
    - New SSH key
        - Key文本框里粘贴 **id_rsa.pub** 文件内容

SSH加密：GitHub 用SSH公钥识别是用户自己推送的

GitHub默认公有仓库，创建私有仓库方法

- 方法一：GitHub付费7刀一个月
- 方法二：搭建自己的Git服务器

# 05 Git 远程仓库

**早期：**

- 一台电脑充当服务器，7 x 24 开机
- 别的机器可以克隆原始版本库

**现在：** GitHub（Git仓库托管服务）

本地Git仓库和GitHub仓库之间的传输是通过SSH加密：

1. 创建SSH Key
    - 用户主目录下有没有 **.ssh** 目录
        - **.ssh** 目录下有没有 **id_rsa** 和 **id_rsa.pub** 这两个密钥对。如果有直接去步骤 2
        - **id_rsa**：私钥
        - **id_rsa.pub** ：公钥
    - 用户主目录下没有 **.ssh** 目录
        - 打开 Git Bash 创建SSH Key
```
$ ssh-keygen -t rsa -C "youremail@example.com"
```

2. 登陆Github - Settings - SSH and GPG Keys
    - New SSH key
        - Key文本框里粘贴 **id_rsa.pub** 文件内容

SSH加密：GitHub 用SSH公钥识别是用户自己推送的

GitHub默认公有仓库，创建私有仓库方法

- 方法一：GitHub付费7刀一个月
- 方法二：搭建自己的Git服务器

## 05-01 添加远程库
本地Git仓库和GitHub仓库远程同步

1. 登陆GitHub - New repository
    - Repository name：learngit
    - Create repository
2. 在本地的learngit仓库下运行命令：
```
$ git remote add origin git@github.com:USERNAME/learngit.git
```
origin 是远程库的名字，是Git默认叫法，可以改成别的

3. **git push** 把本地库的所有内容推送到远程库
    - 第一次推送master分支加上 **-u** 参数
    - Git把本地的master分支内容推送的远程新的master分支
    - Git把本地的master分支和远程的master分支关联起来
```
$ git push -u origin master
Counting objects: 16, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (12/12), done.
Writing objects: 100% (16/16), 1.31 KiB | 0 bytes/s, done.
Total 16 (delta 3), reused 0 (delta 0)
remote: Resolving deltas: 100% (3/3), done.
To git@github.com:USERNAME/learngit.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.
```
4. **git push** 把本地master分支的最新修改推送至GitHub
```
$ git push origin master
```
5. **git remote rm origin** 删除远程仓库
```
$ git remote rm origin
```
### SSH警告

第一次使用Git的clone或者push命令连接 GitHub 会得到一个警告：
```
The authenticity of host 'github.com (xx.xx.xx.xx)' can't be established.
RSA key fingerprint is xx.xx.xx.xx.xx.
Are you sure you want to continue connecting (yes/no)?
```
输入yes回车：
```
Warning: Permanently added 'github.com' (RSA) to the list of known hosts.
```
警告目的：防止有人冒充GitHub服务器违法窃取用户提交的文件

## 05-02 与远程仓库连接操作

### 已经建立远程仓库，从零开始新建本地仓库
先创建GitHub仓库再克隆到本地Git

1. 登陆GitHub新建仓库叫gitskills
2. 命令git clone克隆一个本地库

```
$ git clone git@github.com:USERNAME/gitskills.git
$ cd gitskills
$ touch README.md
$ git add README.md
$ git commit -m "add README"
$ git push -u origin master
```
### 已经存在文件夹，并且未建立过远程仓库连接

```
$ cd existing_folder      #切到已存在的目录下
$ git init                #初始化git
$ git remote add origin git@github.com:USERNAME/gitskills.git   #建立远成仓库连接
$ git add .               #添加文件
$ git commit              #提交
$ git push -u origin master   #push到远程仓库
```
### 已经存在本地仓库
```
$ cd existing_repository_folder       #切到已存在的git分支的目录下
$ rm -rf .git                         #删除该分支之前的git配置
$ git init                            #初始化git
$ git remote add origin git@github.com:USERNAME/gitskills.git   #建立新的远成仓库连接
$ git add .                         #添加文件
$ git commit                        #提交
$ git push -u origin master         #push到远程仓库
```

# 06 Git 分支管理

分支作用：

- 主分支不能一直在修改（会导致项目中其他人不能干活）
- 主分支不能一次性推送（会导致一个篮子里鸡蛋都碎了）
- 创建一个新分支
    - 在新分支中工作
    - 随时提交
    - 开发完合并到Master Branch


## 06-01 创建与合并分支
![image](https://www.liaoxuefeng.com/files/attachments/0013849087937492135fbf4bbd24dfcbc18349a8a59d36d000/0)
1. 创建分支
```
$ git branch dev
```
2. 切换分支
```
$ git checkout dev
Switched to branch 'dev'
```
第一第二步可以合并成一句：
```
$ git checkout -b dev
Switched to a new branch 'dev'
```
![image](https://www.liaoxuefeng.com/files/attachments/001384908811773187a597e2d844eefb11f5cf5d56135ca000/0)

3. 查看当前分支
    - 当前分支前有星号
```
$ git branch
* dev
  master
```
4. 修改readme.txt文件并提交到当前分支
```
Creating a new branch is quick.
```
```
$ git add readme.txt 
$ git commit -m "branch test"
[dev fec145a] branch test
 1 file changed, 1 insertion(+)
```
![image](https://www.liaoxuefeng.com/files/attachments/0013849088235627813efe7649b4f008900e5365bb72323000/0)

5. 切换回master分支
```
$ git checkout master
Switched to branch 'master'
```
![image](https://www.liaoxuefeng.com/files/attachments/001384908892295909f96758654469cad60dc50edfa9abd000/0)

6. 合并dev分支到master分支
```
$ git merge dev
Updating d17efd8..fec145a
Fast-forward
 readme.txt |    1 +
 1 file changed, 1 insertion(+)
```
![image](https://www.liaoxuefeng.com/files/attachments/00138490883510324231a837e5d4aee844d3e4692ba50f5000/0)

7. 删除dev分支
```
$ git branch -d dev
Deleted branch dev (was fec145a).
```
![image](https://www.liaoxuefeng.com/files/attachments/001384908867187c83ca970bf0f46efa19badad99c40235000/0)

## 06-02 解决冲突
两个分支的同一个文件做了不同修改导致 **冲突**

feature1分支修改readme.txt

```
$ git checkout -b feature1
Switched to a new branch 'feature1'
```
```
Creating a new branch is quick AND simple.
```
```
$ git add readme.txt 
$ git commit -m "AND simple"
[feature1 75a857c] AND simple
 1 file changed, 1 insertion(+), 1 deletion(-)
```
master分支修改readme.txt
```
$ git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 1 commit.
```
```
Creating a new branch is quick & simple.
```
```
$ git add readme.txt 
$ git commit -m "& simple"
[master 400b400] & simple
 1 file changed, 1 insertion(+), 1 deletion(-)
```
master分支和feature1分支各自都分别有新的提交

![image](https://www.liaoxuefeng.com/files/attachments/001384909115478645b93e2b5ae4dc78da049a0d1704a41000/0)

此时合并会产生**冲突**

```
$ git merge feature1
Auto-merging readme.txt
CONFLICT (content): Merge conflict in readme.txt
Automatic merge failed; fix conflicts and then commit the result.
```
直接查看readme.txt的内容：

```
Git is a distributed version control system.
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.
<<<<<<< HEAD
Creating a new branch is quick & simple.
=======
Creating a new branch is quick AND simple.
>>>>>>> feature1
```
修改如下后保存：
```
Creating a new branch is quick and simple.
```
再提交：

```
$ git add readme.txt 
$ git commit -m "conflict fixed"
[master 59bc1cb] conflict fixed
```
![image](https://www.liaoxuefeng.com/files/attachments/00138490913052149c4b2cd9702422aa387ac024943921b000/0)

git log 可以看到分支的合并情况：

```
$ git log --graph --pretty=oneline --abbrev-commit
*   59bc1cb conflict fixed
|\
| * 75a857c AND simple
* | 400b400 & simple
|/
* fec145a branch test
...
```
删除feature1分支：

```
$ git branch -d feature1
Deleted branch feature1 (was 75a857c).
```


## 06-03 分支管理策略

合并分支默认使用Fast forward 模式

Fast Forward 缺点：删除分支后，会丢掉分支信息

### 禁用Fast forward模式

1. 创建并切换dev分支：
```
$ git checkout -b dev
Switched to a new branch 'dev'
```
2. 修改readme.txt文件，并提交一个新的commit：
```
$ git add readme.txt 
$ git commit -m "add merge"
[dev 6224937] add merge
 1 file changed, 1 insertion(+)
```
3. 切换回master：
```
$ git checkout master
Switched to branch 'master'
```
4. 合并dev分支
    - --no-ff参数：禁用Fast forward
    - -m参数：添加commit描述
```
$ git merge --no-ff -m "merge with no-ff" dev
Merge made by the 'recursive' strategy.
 readme.txt |    1 +
 1 file changed, 1 insertion(+)
```
![image](https://www.liaoxuefeng.com/files/attachments/001384909222841acf964ec9e6a4629a35a7a30588281bb000/0)

### 分支策略
![image](https://www.liaoxuefeng.com/files/attachments/001384909239390d355eb07d9d64305b6322aaf4edac1e3000/0)

- master分支：只用来发布新版本，不用来开发
    - dev分支：用来开发
        - 每个人在dev分支上开发，每个人都有自己的分支，时不时往dev分支上合并

## 06-04 存储工作区
git stash存储当前工作区
```
$ git stash
Saved working directory and index state WIP on dev: 6224937 add merge
HEAD is now at 6224937 add merge
```
git stash list查看存储的工作区：
```
$ git stash list
stash@{0}: WIP on dev: 6224937 add merge
```
恢复方法一：git stash apply

- stash内容不删除
- git stash drop手动删除

恢复方法二：git stash pop

- stash内容恢复后删除

```
$ git stash pop
# On branch dev
# Changes to be committed:
#   (use "git reset HEAD <file>..." to unstage)
#
#       new file:   hello.py
#
# Changes not staged for commit:
#   (use "git add <file>..." to update what will be committed)
#   (use "git checkout -- <file>..." to discard changes in working directory)
#
#       modified:   readme.txt
#
Dropped refs/stash@{0} (f624f8e5f082f2df2bed8a4e09c12fd2943bdd40)
```

## 06-05 Feature分支
新建一个新功能分支，开发完再合并到master branch
```
$ git checkout -b feature-vulcan
Switched to a new branch 'feature-vulcan'
```
开发完毕
```
$ git add vulcan.py
$ git status
# On branch feature-vulcan
# Changes to be committed:
#   (use "git reset HEAD <file>..." to unstage)
#
#       new file:   vulcan.py
#
$ git commit -m "add feature vulcan"
[feature-vulcan 756d4af] add feature vulcan
 1 file changed, 2 insertions(+)
 create mode 100644 vulcan.py
```
切回dev，准备合并：
```
$ git checkout dev
```
突然要销毁该分支

```
$ git branch -d feature-vulcan
error: The branch 'feature-vulcan' is not fully merged.
If you are sure you want to delete it, run 'git branch -D feature-vulcan'.
```
删不了，只能强制删除
```
$ git branch -D feature-vulcan
Deleted branch feature-vulcan (was 756d4af).
```

## 06-06 多人协作

git remote 查看远程仓库信息
```
$ git remote
origin
```
git remote -v 查看详细远程仓库信息
```
$ git remote -v
origin  git@github.com:USERNAME/learngit.git (fetch)
origin  git@github.com:USERNAME/learngit.git (push)
```
### 推送分支
推送master branch
```
$ git push origin master
```
推送dev branch
```
$ git push origin dev
```
分支种类

- master branch：时刻与远程同步
- dev branch：时刻与远程同步
- bug branch：只用于在本地修复bug，不需要推送
- feature

### 抓取分支

同事A克隆了仓库
```
$ git clone git@github.com:michaelliao/learngit.git
Cloning into 'learngit'...
remote: Counting objects: 46, done.
remote: Compressing objects: 100% (26/26), done.
remote: Total 46 (delta 16), reused 45 (delta 15)
Receiving objects: 100% (46/46), 15.69 KiB | 6 KiB/s, done.
Resolving deltas: 100% (16/16), done.
```
同事A只能看到master branch
```
$ git branch
* master
```
同事A要在dev分支上开发必须创建origin的dev分支到本地
```
$ git checkout -b dev origin/dev
```
同事A把dev分支push到远程：
```
$ git commit -m "add /usr/bin/env"
[dev 291bea8] add /usr/bin/env
 1 file changed, 1 insertion(+)
$ git push origin dev
Counting objects: 5, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 349 bytes, done.
Total 3 (delta 0), reused 0 (delta 0)
To git@github.com:USERNAME/learngit.git
   fc38031..291bea8  dev -> dev
```
同事B对同样的文件作了修改，并试图推送：
```
$ git add hello.py 
$ git commit -m "add coding: utf-8"
[dev bd6ae48] add coding: utf-8
 1 file changed, 1 insertion(+)
$ git push origin dev
To git@github.com:USERNAME/learngit.git
 ! [rejected]        dev -> dev (non-fast-forward)
error: failed to push some refs to 'git@github.com:USERNAME/learngit.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Merge the remote changes (e.g. 'git pull')
hint: before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
推送失败，必须先
用git pull把最新的提交从origin/dev抓下来，然后，在本地合并，解决冲突，再推送：
```
$ git pull
remote: Counting objects: 5, done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 3 (delta 0)
Unpacking objects: 100% (3/3), done.
From github.com:michaelliao/learngit
   fc38031..291bea8  dev        -> origin/dev
There is no tracking information for the current branch.
Please specify which branch you want to merge with.
See git-pull(1) for details

    git pull <remote> <branch>

If you wish to set tracking information for this branch you can do so with:

    git branch --set-upstream dev origin/<branch>
```
git pull也失败，原因是没有指定本地dev分支与远程origin/dev分支的链接，先设置dev和origin/dev的链接：
```
$ git branch --set-upstream dev origin/dev
Branch dev set up to track remote branch dev from origin.
```
再pull：

```
$ git pull
Auto-merging hello.py
CONFLICT (content): Merge conflict in hello.py
Automatic merge failed; fix conflicts and then commit the result.
```
这回git pull成功，但是合并有冲突，需要手动解决，解决的方法和分支管理中的解决冲突完全一样。解决后，提交，再push：
```
$ git commit -m "merge & fix hello.py"
[dev adca45d] merge & fix hello.py
$ git push origin dev
Counting objects: 10, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (5/5), done.
Writing objects: 100% (6/6), 747 bytes, done.
Total 6 (delta 0), reused 0 (delta 0)
To git@github.com:michaelliao/learngit.git
   291bea8..adca45d  dev -> dev
```
多人协作 工作模式

- 用git push origin branch-name推送自己的修改
- 如果推送失败，则因为远程分支比你的本地更新，需要先用git pull试图合并
- 如果合并有冲突，则解决冲突，并在本地提交
- 没有冲突或者解决掉冲突后，再用git push origin branch-name推送就能成功

# 07 Git 标签管理

标签（tag）：和commit绑定在一起的有意义的名字

## 07-01 创建标签

### 07-01-01 默认标签（打在最新提交的commit上）
1. 切换到需要打标签的分支
```
$ git branch
* dev
  master
$ git checkout master
Switched to branch 'master'
```
2. git tag <name> 新建标签
```
$ git tag v1.0
```
3. git tag 查看所有标签
```
$ git tag
v1.0
```
### 07-01-02 指定 Commit ID 标签
1. 找到历史提交的commit id
```
$ git log --pretty=oneline --abbrev-commit
6a5819e merged bug fix 101
cc17032 fix bug 101
7825a50 merge with no-ff
6224937 add merge
59bc1cb conflict fixed
400b400 & simple
75a857c AND simple
fec145a branch test
d17efd8 remove test.txt
...
```
2. 给指定Commit打标签
```
$ git tag v0.9 6224937
```
3. git tag 查看所有标签
```
$ git tag
v0.9
v1.0
```
### 07-01-03 指定 Commit ID 和标签信息的标签
```
$ git tag -a v0.1 -m "version 0.1 released" 3628164
```
### 07-01-04 指定 Commit ID 和 PGP签名 的标签
```
$ git tag -s v0.2 -m "signed version 0.2 released" fec145a
```
## 07-02 操作标签

### 07-02-01 删除本地标签

```
$ git tag -d v0.1
Deleted tag 'v0.1' (was e078af9)
```

### 07-02-02 推送本地标签
git push origin <tagname>：
```
$ git push origin v1.0
Total 0 (delta 0), reused 0 (delta 0)
To git@github.com:USERNAME/learngit.git
 * [new tag]         v1.0 -> v1.0
```
### 07-02-03 推送全部标签
git push origin --tags
```
$ git push origin --tags
Counting objects: 1, done.
Writing objects: 100% (1/1), 554 bytes, done.
Total 1 (delta 0), reused 0 (delta 0)
To git@github.com:USERNAME/learngit.git
 * [new tag]         v0.2 -> v0.2
 * [new tag]         v0.9 -> v0.9
```
### 07-02-04 删除远程标签
1. 先从本地删除
```
$ git tag -d v0.9
Deleted tag 'v0.9' (was 6224937)
```

2. 再从远程删除
```
$ git push origin :refs/tags/v0.9
To git@github.com:USERNAME/learngit.git
 - [deleted]         v0.9
```
# 08 Git 使用GitHub

GitHub让项目开源并且可以让所有人都参与到项目的开发中

例：参与bootstrap项目

1. Fork 在自己账号下克隆一个bootstrap仓库

2. 从自己账号下clone到本地
```
git clone git@github.com:USERNAME/bootstrap.git
```
![image](https://www.liaoxuefeng.com/files/attachments/001384926554932eb5e65df912341c1a48045bc274ba4bf000/0)

**注意：** 只有从自己账号下clone才能推送修改，直接从git@github.com:twbs/bootstrap.git克隆不能推送修改

如果要官方接受修改则需要pull request

# 09 Git 自定义Git

让Git显示颜色：
```
$ git config --global color.ui true
```

## 09-01 忽略特殊文件
在工作区根目录下创建.gitignore文件，把需要忽略的文件名填进去，Git会自动忽略这些文件

不需要从头写.gitignore文件，GitHub已经为我们准备了各种配置文件，只需要组合一下就可以使用了。所有配置文件可以直接[在线浏览](https://github.com/github/gitignore)

忽略文件的原则：

- 忽略操作系统自动生成的文件
- 忽略编译生成的中间文件、可执行文件等
    - 一个文件是通过另一个文件自动生成的，那自动生成的文件就没必要放进版本库（比如Java编译产生的.class文件）
- 忽略带有敏感信息的配置文件，比如存放口令的配置文件


## 09-02 配置别名
把 git status 改成 git st

```
$ git config --global alias.st status
```
用co表示checkout，ci表示commit，br表示branch：
```
$ git config --global alias.co checkout
$ git config --global alias.ci commit
$ git config --global alias.br branch
```

### 配置文件
Git配置文件都放在.git/config文件中：
```
$ cat .git/config 
[core]
    repositoryformatversion = 0
    filemode = true
    bare = false
    logallrefupdates = true
    ignorecase = true
    precomposeunicode = true
[remote "origin"]
    url = git@github.com:michaelliao/learngit.git
    fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
    remote = origin
    merge = refs/heads/master
[alias]
    last = log -1
```
当前用户的Git配置文件放在用户主目录下的一个隐藏文件.gitconfig中：
```
$ cat .gitconfig
[alias]
    co = checkout
    ci = commit
    br = branch
    st = status
[user]
    name = Your Name
    email = your@email.com
```
配置别名也可以直接修改这个文件，如果改错了，可以删掉文件重新通过命令配置。

## 09-03 搭建Git服务器

不想开源又不想给GitHub付钱则自己搭建Git服务器

必须是Linux系统

1. 安装Git
```
$ sudo apt-get install git
```
2. 创建一个git用户，用来运行git服务：
```
$ sudo adduser git
```
3. 创建证书登录：
    - 收集所有需要登录的用户的公钥（每个用户的id_rsa.pub文件）
    - 把所有公钥导入到/home/git/.ssh/authorized_keys文件里，一行一个
4. 初始化Git仓库
    - 选定一个目录作为Git仓库，假定是/srv/sample.git，在/srv目录下输入命令：
```
$ sudo git init --bare sample.git
```
Git就会创建一个裸仓库，裸仓库没有工作区，因为服务器上的Git仓库纯粹是为了共享，所以不让用户直接登录到服务器上去改工作区，并且服务器上的Git仓库通常都以.git结尾。然后，把owner改为git：
```
$ sudo chown -R git:git sample.git
```
5. 禁用shell登录：

出于安全考虑，第二步创建的git用户不允许登录shell，这可以通过编辑/etc/passwd文件完成。找到类似下面的一行：
```
git:x:1001:1001:,,,:/home/git:/bin/bash
```
改为：
```
git:x:1001:1001:,,,:/home/git:/usr/bin/git-shell
```
这样，git用户可以正常通过ssh使用git，但无法登录shell，因为我们为git用户指定的git-shell每次一登录就自动退出。

6. 克隆远程仓库：
    - 通过 git clone 克隆远程仓库，在各自的电脑上运行：
```
$ git clone git@server:/srv/sample.git
Cloning into 'sample'...
warning: You appear to have cloned an empty repository.
```