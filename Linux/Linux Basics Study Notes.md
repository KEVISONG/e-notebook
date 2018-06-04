# Linux Basics Study Notes
> By Kevin Song

<!-- MarkdownTOC autolink='true' -->

- [01 操作系统基础](#01-%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F%E5%9F%BA%E7%A1%80)
- [02 Linux 系统基础](#02-linux-%E7%B3%BB%E7%BB%9F%E5%9F%BA%E7%A1%80)
	- [02-01 文件系统](#02-01-%E6%96%87%E4%BB%B6%E7%B3%BB%E7%BB%9F)
	- [02-02 命令格式与帮助](#02-02-%E5%91%BD%E4%BB%A4%E6%A0%BC%E5%BC%8F%E4%B8%8E%E5%B8%AE%E5%8A%A9)
- [03 Linux 常用命令](#03-linux-%E5%B8%B8%E7%94%A8%E5%91%BD%E4%BB%A4)
	- [03-01 基础命令\(ls, cd\)](#03-01-%E5%9F%BA%E7%A1%80%E5%91%BD%E4%BB%A4ls-cd)
	- [03-02 创建和删除\(touch, mkdir, rm\)](#03-02-%E5%88%9B%E5%BB%BA%E5%92%8C%E5%88%A0%E9%99%A4touch-mkdir-rm)
	- [03-03 拷贝和移动\(tree, cp, mv\)](#03-03-%E6%8B%B7%E8%B4%9D%E5%92%8C%E7%A7%BB%E5%8A%A8tree-cp-mv)
	- [03-04 查看文件内容\(cat, more, grep\)](#03-04-%E6%9F%A5%E7%9C%8B%E6%96%87%E4%BB%B6%E5%86%85%E5%AE%B9cat-more-grep)
	- [03-05 其他\(echo, 重定向, 管道\)](#03-05-%E5%85%B6%E4%BB%96echo-%E9%87%8D%E5%AE%9A%E5%90%91-%E7%AE%A1%E9%81%93)
- [04 Linux 远程管理](#04-linux-%E8%BF%9C%E7%A8%8B%E7%AE%A1%E7%90%86)
	- [04-01 关机重启\(shutdown\)](#04-01-%E5%85%B3%E6%9C%BA%E9%87%8D%E5%90%AFshutdown)
	- [04-02 查看配置网卡信息\(ifconfig, ping\)](#04-02-%E6%9F%A5%E7%9C%8B%E9%85%8D%E7%BD%AE%E7%BD%91%E5%8D%A1%E4%BF%A1%E6%81%AFifconfig-ping)
	- [04-03 远程登陆和复制文件\(ssh, scp\)](#04-03-%E8%BF%9C%E7%A8%8B%E7%99%BB%E9%99%86%E5%92%8C%E5%A4%8D%E5%88%B6%E6%96%87%E4%BB%B6ssh-scp)
- [05 Linux 用户和权限](#05-linux-%E7%94%A8%E6%88%B7%E5%92%8C%E6%9D%83%E9%99%90)
	- [05-01 用户权限和组基本概念\(r, w, x, sudo\)](#05-01-%E7%94%A8%E6%88%B7%E6%9D%83%E9%99%90%E5%92%8C%E7%BB%84%E5%9F%BA%E6%9C%AC%E6%A6%82%E5%BF%B5r-w-x-sudo)
	- [05-02 组管理命令\(groupadd, groupdel\)](#05-02-%E7%BB%84%E7%AE%A1%E7%90%86%E5%91%BD%E4%BB%A4groupadd-groupdel)
	- [05-03 用户管理命令\(useradd, passwd, userdel, id, who, whoami, usermod, su\)](#05-03-%E7%94%A8%E6%88%B7%E7%AE%A1%E7%90%86%E5%91%BD%E4%BB%A4useradd-passwd-userdel-id-who-whoami-usermod-su)
	- [05-04 修改权限命令\(chown, chgrp, chmod\)](#05-04-%E4%BF%AE%E6%94%B9%E6%9D%83%E9%99%90%E5%91%BD%E4%BB%A4chown-chgrp-chmod)
- [06 Linux 系统信息](#06-linux-%E7%B3%BB%E7%BB%9F%E4%BF%A1%E6%81%AF)
	- [06-01 时间和日期\(date, cal\)](#06-01-%E6%97%B6%E9%97%B4%E5%92%8C%E6%97%A5%E6%9C%9Fdate-cal)
	- [06-02 磁盘和目录空间\(df, du\)](#06-02-%E7%A3%81%E7%9B%98%E5%92%8C%E7%9B%AE%E5%BD%95%E7%A9%BA%E9%97%B4df-du)
	- [06-03 进程查看排序终止\(ps, top, kill\)](#06-03-%E8%BF%9B%E7%A8%8B%E6%9F%A5%E7%9C%8B%E6%8E%92%E5%BA%8F%E7%BB%88%E6%AD%A2ps-top-kill)
- [07 Linux 其他命令](#07-linux-%E5%85%B6%E4%BB%96%E5%91%BD%E4%BB%A4)
	- [07-01 查找文件\(find\)](#07-01-%E6%9F%A5%E6%89%BE%E6%96%87%E4%BB%B6find)
	- [07-02 软连接\(ln\)](#07-02-%E8%BD%AF%E8%BF%9E%E6%8E%A5ln)
	- [07-03 打包和压缩\(tar\)](#07-03-%E6%89%93%E5%8C%85%E5%92%8C%E5%8E%8B%E7%BC%A9tar)
	- [07-04 软件安装\(apt\)](#07-04-%E8%BD%AF%E4%BB%B6%E5%AE%89%E8%A3%85apt)
- [08 附件](#08-%E9%99%84%E4%BB%B6)

<!-- /MarkdownTOC -->


# 01 操作系统基础
操作系统作用
- 直接操作硬件
- 把操作硬件的代码封装成系统调用（System Call），供程序员通过系统调用间接操作硬件

四种主流操作系统
- 桌面操作系统（Windows，MacOS，Linux）
- 服务器操作系统（Linux，Windows Server）
- 嵌入式操作系统（Linux）
- 移动设备操作系统（iOS，Android）

# 02 Linux 系统基础

## 02-01 文件系统
每个用户有自己的目录，共享计算机资源
- / 根目录
    - /home 家目录
        - /home/KEVISONG 用户家目录，**用~表示**
            - ~/Documents 
            - ~/Desktop

符号 | 含义
---|---
. | 当前目录
.. | 上一级目录
~ | 用户家目录
## 02-02 命令格式与帮助
**命令格式**
```
command [-option] [parameter]
command：     命令名
[-option]：   选项，可用来对命令进行控制
[parameter]： 传递给命令的参数，可以是零个，一个，或者多个
[]            中括号表示可选，没有中括号表示必选
```
**帮助信息**
- 方法一：command --help
- 方法二：man command

按键 | 含义
---|---
空格 | 显示手册下一屏
Enter | 向下滚动一行
b | 回滚一屏
f | 前滚一屏
q | 退出

**自动补全**

```
cd De		//按一次tab可以自动补全
cd Desktop
```
如果有多种选择可能
```
cd Do		//按两次tab可以显示所有可能
Documents/  Downloads/
```
**命令选择技巧**

- ↑↓查看历史命令
- ctrl + c 恢复

# 03 Linux 常用命令

## 03-01 基础命令(ls, cd)
**ls 列出文件**
```
ls
123.txt
ls -a   //显示所有文件
123.txt .123.txt
```
参数|含义
---|---
-a | 显示所有目录和文件，包括隐藏文件
-l | 以列表的方式显示文件的详细信息
-h | 配合-l以人性化的方式显示文件大小

```
ls -l
drwxrwxr-x 2 python python 4096 7 30 2016 dbs
-rw-r--r-- 1 python python 8980 5 16 2016 examples.desktop
ls -l -h	//或者ls -lh
drwxrwxr-x 2 python python 4.0K 7 30 2016 dbs
-rw-r--r-- 1 python python 8.8K 5 16 2016 examples.desktop
```
ls配合通配符的使用

通配符 | 含义
---|---
\* | 任意个数字符
\? | 任意一个字符，至少1个
\[\] | 字符组种任意1个
\[abc\] | a，b，c中任意一个
\[a\-d\] | a-d中任意一个

**cd 切换目录**

命令 | 含义
---|---
cd | 切换到当前用户的主目录（/home/用户目录）
cd ~ | 切换到当前用户的主目录（/home/用户目录）
cd . | 保持当前目录
cd .. | 切换上级目录
cd - | 最近两个目录间切换

**相对路径**：输入路径时，最前面不是/或者~，表示相对 **当前目录** 所在的目录位置  
**绝对路径**：输入路径时，最前面是/或者~，表示从 **根目录/家目录** 开始的具体目录位置

## 03-02 创建和删除(touch, mkdir, rm)
**touch 创建文件**

```
touch 文件名
touch 123.txt
```
- 文件已存在：修改文件最后修改时间
- 文件不存在：创建空白文件


**mkdir 创建目录**
```
mkdir 目录名
mkdir 123
```
选项 | 含义
---|---
-p | 递归创建目录
```
mkdir -p a/b/c/d
```

**rm 删除文件或目录**

```
rm -rf *    //刺激
```

选项 | 含义
---|---
-f | 强制删除，忽略不存在的文件，无需提示
-r | 递归删除目录，删除文件夹时必选
> rm删除的文件无法恢复

## 03-03 拷贝和移动(tree, cp, mv)
**tree 以树状图列出文件目录结构**
```
tree [文件名]
tree ~/
```
选项 | 含义
---|---
-d | 只显示目录

**cp 复制文件**

```
cp  源文件                  目标文件
cp  ~/Documents/readme.txt  ./readme.txt
```
选项 | 含义
---|---
-i | 询问是否覆盖已存在文件，用y和n回答
-r | 递归复制目录，目标文件必须是一个目录

**mv 移动文件**

```
mv  源文件                  目标文件
mv  ~/Documents/readme.txt  ./readme.txt    //仅移动
mv  ~/Documents/readme.txt  ~/Documents/readme666.txt //移动并且重命名
```
选项 | 含义
---|---
-i | 询问是否覆盖已存在文件，用y和n回答
> 推荐使用-i选项，可以防止已经存在的文件被覆盖

## 03-04 查看文件内容(cat, more, grep)
**cat（适合内容少的文本）查看文件内容，创建文件，文件合并，追加文件内容**  

```
cat 文件名
cat 123.txt
```
选项 | 含义
---|---
-b | 对非空输出行编号（nl命令效果等价）
-n | 对所有输出行编号


**more（适合内容多的文本）分屏显示文件内容**
```
more 文件名
more 123.txt
```
> 操作方式和man一样


**grep 对文本文件进行模式查找并打印**

```
grep 查找内容 文件名
grep Rise Rising.txt
grep "Hi there" Hi.txt
```
选项 | 含义
---|---
-n | 显示匹配行和行号
-v | 显示不包含匹配文本的所有行
-i | 忽略大小写
模式匹配
```
grep ^K 123.txt //以K开头
grep K$ 123.txt //以K结尾
```

## 03-05 其他(echo, 重定向, 管道)
**echo 在终端中显示文字**
```
echo 文字
echo Hello
```



**重定向 > 和 >>**

把本应该输出到终端的内容 **输出 >** 或 **追加 >>** 到文件中

```
echo Hello > a	// 输出到a文件，覆盖原有内容
echo Linux >> a	// 追加到a文件
```
> 如果文件不存在则创建文件并输出或追加内容



**管道 |**

一个命令的输出通过 **管道 |** 作为另一个命令的输入

```
命令 | 命令
ls -lh | more	//列出所有文件 并 分屏显示
ls -lh | grep Do//列出所有文件 并 搜索Do
```
# 04 Linux 远程管理

## 04-01 关机重启(shutdown)
```
shutdown 时间
shutdown        //不指定时间默认1分钟之后关机
shutdown now    //立即关机
shutdown +10    //10分钟后关机
shutdown 20:25  //20：25关机
```
选项 | 含义
---|---
-r | 重启
-c | 取消关机

```
shutdown -r now
shutdown -c
```
## 04-02 查看配置网卡信息(ifconfig, ping)
**ifconfig 查看、配置计算机的网卡配置信息**

```
ifconfig
ifconfig | grep inet    //查看ip地址
```



**ping** 

```
ping ip地址
ping 127.0.0.1
ctrl + c 结束
```
## 04-03 远程登陆和复制文件(ssh, scp)
**ssh (Secure Shell) 远程登陆**  

**SSH协议**：远程登陆会话和其他网络服务安全性协议  
**作用**：用SSH客户端**远程登陆**运行SSH服务器（端口号22）的远程机器  
**优点**：1.数据加密，防止泄露 2.数据压缩，传输提速  
**原理**：
- 通过**IP地址**找到网络上的**计算机**
- 通过**端口号**找到计算机上的**应用程序**

```
ssh [-p 端口号] 用户名@远程机器地址
ssh -p 22 ksong@192.168.1.3
```
- 用户名：电脑上的用户名
- 主机地址：可以是IP、域名、别名
- 端口号：SSH服务器监听的端口，不指定则默认22
- exit 退出登录

> Windows需要安装PuTTY或XShell才能远程登陆


**scp (Secure Copy) 远程复制**

```
scp [-P 端口] 本地文件名 用户名@远程机器地址:远程目录/远程文件
scp -P 22 01.py ksong@192.168.1.3:Desktop/01.py   //本地 > 服务器
scp [-P 端口] 用户名@远程机器地址:远程目录/远程文件 本地文件名
scp -P 22 ksong@192.168.1.3:Desktop/01.py 01.py   //服务器 > 本地
```
> ：后路径如果不是绝对路径，则默认为用户家目录

选项 | 含义
---|---
-r | 传递文件夹
-P | 指定SSH 服务器端口号

```
scp -P 22 -r demodir ksong@192.168.1.3:Desktop    //本地 > 服务器
scp -P 22 -r ksong@192.168.1.3:Desktop demodir    //服务器 > 本地
```
**ssh 配置免密码登陆（非对称加密算法）**

```
ssh-keygen 生成SSH钥匙对
ssh-keygen
ssh-copy-id -p port user@remote 把公钥发给服务器
ssh-copy-id -p 22 ksong@192.168.1.3
```
- 公钥 id_rsa.pub 服务器用来加密解密数据
- 私钥 id_rsa     客户端用来加密解密数据

> SSH配置信息保存在用户家目录下的 **.ssh** 目录

**ssh 配置别名（修改~/.ssh/config文件）**
ssh ksong@192.168.1.3
~/.ssh/config中追加以下内容
```
Host KEVISONG
    HostName 192.168.1.3
    User ksong
    port 22
ssh KEVISONG
```
# 05 Linux 用户和权限

## 05-01 用户权限和组基本概念(r, w, x, sudo)

**用户、权限、组**

每一个用户对不同的文件或目录有不同的读写权限

权限 | 英文 | 缩写 | 数字代号
---|---|---|---
读 | read | r | 4
写 | write | w | 2
执行 | excute | x | 1

**组(Group)**：不同用户放入不同组中，方便管理

**ls -l 详解**  

<font face="courier New">ls -l  
d<font color="red">rwx</font><font color="blue">rwx</font>r-x 2 <font color="red">python</font> <font color="blue">python</font> 4096 7 30 2016 dbs  
-<font color="red">rw-</font><font color="blue">r--</font>r-- 1 <font color="red">python</font> <font color="blue">python</font> 8980 5 16 2016 examples.desktop
</font>  
权限 硬链接数 所有者  组名     大小 创建修改时间 文件名

标记|<font color='red'>用户权限</font>|<font color='blue'>组权限|其他用户权限
---|---|---|---
d|<font color='red'>r w x</font>|<font color='blue'>r w x</font>|r - x
-|<font color='red'>r w -</font>|<font color='blue'>r - -</font>|r - -

第一位字母作为标记

字母 | 标记文件
---|---
\- | 普通文件
d | 目录文件
p | 管理文件
l | 链接文件
b | 块设备文件
c | 字符设备文件
s | 套接字文件

硬链接数：访问到这个文件或者目录的方式数

```
方法一：cd /home/python/Desktop/dbs
方法二：cd .
```
> 硬链接数 **-2** 就是子目录数

**超级用户**

root账号：有所有访问权限，用于系统级维护和管理（增删用户组，权限管理，应用管理等）不推荐直接使用

sudo(substitute user do)：用另一个用户身份（默认root）做。暂时提升权限。

```
sudo chmod -rw 01.py
```
- 第一次sudo要输入密码，之后有5分钟有效期
- 未经授权的用户用sudo会发送警告邮件给管理员

## 05-02 组管理命令(groupadd, groupdel)

- 组信息保存在 /etc/group 文件中
    - /etc 目录专门保存系统配置信息
- 创建组或删除组需要sudo

命令|作用
---|---
groupadd 组名 | 添加组
groupdel 组名 | 删除组
cat /etc/group | 确认组信息
chgrp 组名 文件/目录名 | 修改文件/目录所属的组
chgrp -R 组名  文件/目录名 | 递归修改文件/目录所属的组

```
sudo groupadd dev
sudo groupdel dev
drwxrwxr-x 2 python python 4096 7 30 2016 myPy
sudo chgrp -R dev myPy
drwxrwxr-x 2 python dev    4096 7 30 2016 myPy
```

## 05-03 用户管理命令(useradd, passwd, userdel, id, who, whoami, usermod, su)
> 创建用户，设置密码，删除用户 需要sudo

**创建用户(useradd)，设置密码(passwd)，删除用户(userdel)**

命令 | 作用 | 说明
---|---|---
useradd -m -g 组 新建用户名 | 添加新用户 | -m 自动建立用户家目录<br>-g 指定用户所在组，否则建立一个同名组
passwd 用户名 | 设置用户密码 | 普通用户用passwd修改自己密码
userdel -r 用户名 | 删除用户 | -r 自动删除用户家目录
cat /etc/passwd \| grep 用户名 | 确认用户信息 | 用户信息保存在/etc/passwd中

```
sudo useradd -m -g dev ksong
sudo passwd ksong
```

**id, who, whoami 查看用户和组信息**

> /etc/group 保存 组信息 

```
cat -n /etc/group | grep dev
行号 组名 : 密码 : 组ID : 组成员
 5  plugdev:x:46:python
18  nerdev:x:109:
67  dev:x:1001:
```
> /etc/passwd 保存 用户信息 

```
cat -n /etc/passwd | grep ksong
行号 用户名:密码:用户ID:组ID:用户全名:家目录:登陆使用的Shell（ubantu默认是dash）
50  ksong:1002:1001::/home/ksong:
```

命令 | 作用
---|---
id [用户名] |查看用户UID，GID信息，所属组
who |查看当前所有登陆的用户列表
whoami |查看当前目录用户的帐户名

```
id ksong
uid=1002(ksong) gid=1001(dev) 组=1001(dev)
who
python	tty7	2018-03-18 08:29 (:0)//代表当前计算机
ksong	pts/18	2018-03-18 07:16 (172.16.140.133)
whoami
python
```
**usermod 设置组和Shell**
- 主组： **gid** 对应的组
- 附加组： **组\=** 后面对应的组，指定用户的附加权限
```
cat -n /etc/group | grep python
21  sudo:x:27:python	//这个python是用户
67  python:x:1000:	//这个python是组
```
- python 在 sudo 附加组里，所以python可以使用 sudo 命令
- ksong 不在所以不能使用 sudo 命令
```
修改用户主组
usermod -g 组     用户名
usermod -g python ksong
修改用户附加组
usermod -G 组   用户名
usermod -G sudo ksong
修改用户登陆 Shell
usermod -s Shell名   用户名
usermod -s \bin\bash ksong
```
**which 查看命令位置**

```
which 命令
which passwd		which useradd
/usr/bin/passwd		/usr/sbin/useradd
```

Linux中，绝大多数可执行文件保存在/bin、/sbin、/usr/bin、/usr/sbin
- /bin（binary）：二进制执行文件目录，主要用于具体应用
- /sbin（system binary）：系统管理员专用二进制代码存放目录，主要用于系统管理
- /usr/bin（user commands for applications）：后期安装的应用
- /usr/sbin（super user commands for application）：超级用户的管理程序

**su 切换用户**
命令 | 作用
---|---
su - 用户名 | 切换用户，-自动切换到家目录
exit | 删除组

```
python@ubuntu:~$ su - ksong
ksong@ubuntu:~$ exit
python@ubuntu:~$ su -	//不加用户名切换到root
root@ubuntu:~$
```
## 05-04 修改权限命令(chown, chgrp, chmod)
命令 | 作用
---|---
<font color="0000CC">chown | <font color="0000CC">修改拥有者
<font color="CC0000">chgrp | <font color="CC0000">修改组（-R 递归修改）
<font color="00CC00">chmod | <font color="00CC00">修改读写执行权限

**chown 修改文件拥有者**

<font face="courier New"><font color="00CC00">drwxrwxr-x</font> 2 <font color="0000CC">python</font> <font color="CC0000">dev</font> 4096 7 30 2016 myPy</font>
```
chown 用户名 文件/目录名  
chown ksong myPy
```

**chgrp 修改文件组**

<font face="courier New"><font color="00CC00">drwxrwxr-x</font> 2 <font color="0000CC">ksong</font> <font color="CC0000">dev</font> 4096 7 30 2016 myPy //python用户不是所有者，也不在dev组里，所以不可写</font>

```
chgrp 组名 文件/目录名  
chgrp python myPy
```
<font face="courier New"><font color="00CC00">drwxrwxr-x</font> 2 <font color="0000CC">ksong</font> <font color="CC0000">python</font> 4096 7 30 2016 myPy</font>

**chmod 修改权限**

一次性修改拥有者/组/其他用户读写权限  

```
chmod  +/- rwx 文件名或目录名  
chmod -rw 01.py	//移除读写权限  
chmod +rw 01.py	//增加读取权限
```

- 没有 可执行 权限（x）的目录 无法 使用 任何 终端命令：cd ls touch  
- 没有 读 权限（r）的目录 无法 使用 阅读 目录的终端命令：ls  
- 没有 写 权限（w）的目录 无法 使用 修改 目录的终端命令：touch  

针对性修改拥有者/组/其他用户读写权限  
```
chmod 755 01.py //rwxr-xr-x
```


rwx | rw\- | r\-x | r\-\- | \-wx | \-w\- | \-\-x | \-\-\-
---|---|---|---|---|---|---|---
4 |4 | 4| 4 |0 |0 |0 |0  
2 |2 |0 |0 |2 |2 |0 |0  
1 |0 |1 |0 |1 |0 |1 |0  
7 |6 |5 |4 |3 |2 |1 |0  
 

常见组合  

- 777 - u=rwx, g=rwx, o=rwx  
- 755 - u=rwx, g=rx, o=rx  
- 644 - u=rw, g=r, o=r


# 06 Linux 系统信息

## 06-01 时间和日期(date, cal)
**date 查看系统时间**

```
date
```

**cal 查看日历**

```
cal
cal -y
```
选项 | 含义
---|---
-y | 查看一年的日历
## 06-02 磁盘和目录空间(df, du)
**df（disk free）显示磁盘剩余空间**
```
df
df -h
```
选项 | 含义
---|---
-h | 人性化显示大小

**du（disk usage）显示当前目录下的文件大小**

```
du
du -h
```
选项 | 含义
---|---
-h | 人性化显示大小

## 06-03 进程查看排序终止(ps, top, kill)
**ps 查看进程详细状况**

```
ps
 PID	TTY	    TIME	CMD
2587	pts/18	00:00:00	bash
7813	pts/18	00:00:00	ps
ps aux
USER	PID %CPU %MEM   VSZ   RSS TTY	STAT START   TIME COMMAND
root   1290  0.0  3.6 34464 73976 tty7  Ss+  15:22   0:15 /usr/lib/xorg/
```
选项|含义
---|---
a | 显示通过终端启动的所有进程，包括其他用户进程
u | 显示进程的详细状态
x | 显示没有通过终端启动的进程

**top 动态显示运行中的进程，并按CPU内存占用率降序排序**

```
top
按q退出
```

**kill 终止进程**
```
kill PID
kill 9118
kill -9 9118
```
选项 | 含义
---|---
-9 | 强行终止

# 07 Linux 其他命令

## 07-01 查找文件(find)

```
find [路径] -name "*.py"    //省略路径表示在当前目录搜索
find Desktop/ -name "*1*"   //在指定目录搜索
find -name "*1*"            //在当前目录搜索
```

## 07-02 软连接(ln)
**ln -s 建立软连接，类似于 Windows 的快捷方式**

```
ln -s 被链接的源文件 链接文件
ln -s demo/b/c/01.py 01_relative                        //使用相对路径
ln -s /home/python/Desktop/demo/b/c/01.py 01_absolute	//使用绝对路径
```
> 把两个链接文件都移动到demo目录时，使用相对路径建立的软连接不再有效

**原因**：使用相对路径建立软连接时，执行链接文件时用的是组合路径“当前目录+相对路径”，当链接文件目录改变时，新的组合路径与源文件路径不符。  
**结论**：建立软连接时，要用绝对路径

**ln 建立硬链接**

```
ln 被链接的源文件 链接文件
ln /home/python/Desktop/demo/b/c/01.py 01_hard
```

**软连接和硬链接**
> Linux 中 文件名 和 文件数据 分开存放

软链接：
```
graph LR
软链接文件名-->软链接文件数据
软链接文件数据-->文件名
文件名-->文件数据//硬链接数1
```
硬链接：

```
graph LR
硬链接-->文件数据//硬链接数2
文件名-->文件数据//硬链接数2
```
> 硬链接数为 0 时文件数据才会被删除


## 07-03 打包和压缩(tar)
不同系统打包工具不同：
- Windows（rar）
- Mac（zip）
- Linux（tar.gz）

**tar 打包、解包**
```
tar -cvf 打包文件.tar 被打包文件/路径...
tar -cvf py.tar 01.py 02.py 03.py
tar -xvf 打包文件.tar
tar -xvf py.tar
```
选项 | 含义
---|---
-c | 创建打包文件
-x | 解包
-v | 列出详细过程,显示进度
-f | 指定文件名,必须放在最后

**gzip 压缩、解压缩（xxx.tar.gz）**
```
tar -zcvf 打包文件.tar.gz 被打包文件/路径...
tar -zcvf py.tar.gz 01.py 02.py 03.py
tar -zxvf 打包文件.tar.gz
tar -zxvf py.tar.gz
tar -zxvf 打包文件.tar.gz -C 目标路径
tar -zxvf py.tar.gz -C py
```
选项| 含义
---|---
-z | 调用 gzip 进行压缩和解压
-C | 解压缩到指定目录,目标目录必须存在

**bzip2 压缩、解压缩（xxx.tar.bz2）**


```
tar -jcvf 打包文件.tar.bz2 被打包文件/路径...
tar -jcvf py.tar.bz2 01.py 02.py 03.py
tar -jxvf 打包文件.tar.bz2
tar -jxvf py.tar.bz2
```
选项 | 含义
---|---
-j | 调用 bzip2 进行压缩和解压
-C | 解压缩到指定目录，目标目录必须存在

```
tar -zxvf 打包文件.tar.bz2 -C 目标路径
tar -zxvf py.tar.bz2 -C py
```


## 07-04 软件安装(apt)
**apt（Advanced Packaging Tool） 安装/卸载/更新软件包**
安装软件

```
sudo apt install 应用名
sudo apt install htop
```

卸载软件

```
sudo apt remove 应用名
sudo apt remove htop
```

更新已安装的包

```
sudo apt upgrade 应用名
sudo apt upgrade htop
```

**配置软件源**

切换下载的服务器可以提升下载速度
# 08 附件

![image](https://raw.githubusercontent.com/KEVISONG/e-notebooks/master/Linux/pics/ls-l%20details.png)