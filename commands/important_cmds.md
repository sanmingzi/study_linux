# Important commands

```
Ctrl+C
停止进程
```

```
Ctrl+D
结束输入，退出。在 /bin/bash 中按 ctrl+d 可以直接退出
```

```
Ctrl+L
清屏
```

```
man
查看帮助信息
man git # 可以查看git的帮助信息
```

```
echo [字符串][$变量]

echo sanmingzi # 输出字符串
# sanmingzi

echo $SHELL # 输出全局变量
# /bin/zsh

var=1
echo $var # 输出自定义变量
# 1
```

```
date [+指定的格式]

date
# Sat Oct 14 14:21:43 HKT 2023

date "+%Y-%m-%d %H:%M:%S"
# 2023-10-14 14:24:43
```

```
timedatectl
time date control，可设置系统时间
用法：timedatectl [参数]
macos上没有这个命令
```

```
wget
web get，下载。
用法：wget [参数] 网址
-b 后台下载模式
-P 下载到指定目录
-t 最大尝试次数
-c 断点续传
-p 下载页面内所有资源，包括图片、视频等
-r 递归下载

wget -r -p http://www.google.com

该命令可以将 google index.html 以及 images 下载到当前目录下的文件夹 www.google.com 中
cd www.google.com/
ls
# images   index.html   intl   robots.txt
```

```
ps
processes，显示进程
用法：ps [参数]
-a 显示所有进程
-u 显示进程的用户以及其他详细信息
-x 显示没有控制终端的进程

ps aux
```

```
pstree
以树形结构的形式显示进程
```

```
top
```

```
kill 2156 # 杀死进程
kill -9 2156 # 强制杀死进程
killall nginx # 杀死全部进程
```

```
uname
unix name，查看系统内核版本与系统架构信息

uname -a
```

```
uptime
# 16:53  up  8:34, 2 users, load averages: 3.05 2.81 2.66
# 当前时间 系统运行时间 终端数量 系统最近1分钟/5分钟/15分钟内的负载
```

```
free
查看系统内存使用信息

free -h
macos不支持该命令
```

```
who
查看当前登入主机的用户终端信息
who
# root tty Oct 14 08:20
```

```
ping
```

```
netstat
显示网络连接，路由表，接口状态等网络信息
-i 显示网卡列表信息
-r 显示路由表信息
```

```
history
```

```
pwd
print working directory
```

```
cd
change directory

cd - # 回到上一次的目录

cd ~ # 回到当前用户的根目录
```

```
ls
-a 可以查看当前目录下所有文件，包括隐藏文件
-l 显示文件的大小，属性等详细信息
ls -al

ls -ld /etc # 可查看文件夹的属性
# lrwxr-xr-x@ 1 root  wheel  11 Sep 16 15:48 /etc -> private/etc
```

```
tree
以树形结构的形式来显示文件
```

```
find
这个命令很重要，而且有点复杂，有单独介绍
```

```
whereis
可按照名称快速搜索二进制程序的位置

whereis pwd
# pwd: /bin/pwd /usr/share/man/man1/pwd.1
```

```
which
可按照名称快速搜索二进制程序的位置

which postgres
# /usr/local/bin/postgres
```

```
cat
查看纯文本文件（内容较少的）

-n 显示行号
```

```
more
查看纯文本文件（内容较多的），该命令支持翻页等功能
```

```
head
查看纯文本文件的前 N 行

head -n 10 filename # 查看 filename 的前 10 行
```

```
tail
查看纯文本文件的后 N 行或持续刷新文件的最新内容

tail -n 10 filename # 查看 filename 的后 10 行

tail -f filename # 持续刷新 filename 的最新内容
```

```
stat
status，用于查看文件的具体存储细节和时间

stat filename
```

```
cut
提取文件中的列
用法：cut [参数] file
-d 设置分隔符
-f 设置需要提取的列

cut -d : -f 1 test # 将文件 test 的每行用 : 分隔，取第 1 列的内容
```

```
diff
比较文件之间的差异
用法：diff [参数] file0 file1
--brief 显示比较后的结构
-c 显示具体的不同

diff --brief test test0
# Files test and test0 differ

diff -c test test0
```
