# study
## Linux shell

- 基本命令

```
cd 定位主目录
cd folder_name定位指定目录
cp folder_name1 folder_name2复制文本
cp -r 递归复制文本
ls 显示当前目录中的文本和目录
ls -l参数生成长列表格式
ls -il带索引号的长列表格式
touch 新建文本
mv old_name new_name 重命名（移动）
rm -i file_name 询问是否删除文件
rm file_name 不询问直接删除文件
rm -rf folder_name 不询问直接删除整个文件目录
mkdir新建目录
rmdir删除空目录
stat显示除文本类型的详细信息
file显示文本类型
```

- 查看整个文件

```
cat显示文本内容
cat -n 显示带行号的文本内容
more 
less
```
- 监控程序

```
ps 进程查看
ps -ef 扩展输出显示系统上所有运行的程序 
top  实时进程监控
kill/killall 停止进程
command >file 输出重定向
command <file 输入重定向
command1 | command2 管道 命令传入命令
```


echo 在显示器上输出文字

## Markdown语法

前面加1到6个＃，表示1到6级标题

手动换行，在一行中先输入   
3个以上空格后再回车

插入html代码可以直接插入

This is an [example](http://github.com "Github") 行内式  
<http://github.com> 自动链接
This is an [exampel] [1]

[1] http://github.com "example" 参考式

```
区块
```

    或缩进至少4个空格或一个制表符,也是一个区块，作用同上。

详见 http://www.appinn.com/markdown/#p

http://www.appinn.com/markdown/#p

    当我把一个仓库往另一仓库克隆的时候老师都无语了，呵呵～
    初学很痛苦啊，成功很享受啊！
        哥是有追求的人，学习也是一种快乐，很充实！


## git/github

- 格式化代码是什么意思？

- vim 需要安装吗？

- 什么是远程？
查看当前项目下远程
git remote
 增加新的分支链接，例如
git remote add niuren giturl…
 获取牛人的远程更新
git fetch niuren
 将牛人的远程更新合并到本地分支
git merge niuren/master


git fetch branch_name 获取远程分支
git merge branch_name/master 合并远程分支到本地
以上两步相当于
git pull
不同在于修改了多个文件，然后同时进行合并可能会出现很多冲突，这时需要一个文件一个文件的去找冲突，使用上面的两步式就可以每次获取一个文件，合并一个文件，如果有冲突解决冲突在合并。

git clone url包含三步内容
```
git init
git remote add origin url
git pull
```

- iwork应用

- quicksilver软件什么作用？

- zsh中命令补全快捷键

pull request


- 什么是shell
shell是一种交互式的实用程序，它为用户提供了一种启动程序，管理文件系统中的文件，管理运行在Linux 系统中的进程方式。

- vim
vi编辑器处理内存缓冲中的数据。
x或num x 从当前光标位置向后删除
vi 分正常模式和插入模式
dd或 num dd删除当前光标及向下的行
dw num dw 删除单词，原理同上
d$ 删除当前光标到行末，注意不是ds
a变成插入模式并在当前光标后面插入数据 
A变成插入模式并在当前光标所在行末后面插入数据
v 可视模式，可选择要复制的内容
p粘贴
y移出，即复制
删除和剪切类似，删除是把删除的内容放到寄存器中，再执行p粘贴命令即可。
J删除本行断开线
r替换字符,再输入会切换成插入模式
R替换文本，可连续替换
／搜索，n表示下一个
替换
在命令行中:s/sdf(被替换内容)/dfsd(替换内容)
:s/sdf(被替换内容)/dfsd(替换内容)/g替换整行中的
:%（替换全文中的）s/sdf(被替换内容)/dfsd(替换内容)/g
:%s/sdf(被替换内容)/dfsd(替换内容)／gc,替换全文中的，但会依次询问
:num,num s/sdf(被替换内容)/dfsd(替换内容)/g两行（含）之间内容替换。

如果你想要看看你的本地分支里哪些分支是已经合并进你当前所在的分支时，可以使用：
git branch --merged
反过来，如果需要查看哪些分支还没有合并进当前所在的分支，可以使用：
git branch --no-merged
结合高富帅的UNIX工具，你可以轻松的删除那些已经合并了的分支：
git branch --merged | xargs git branch -d
译者注：xargs是UNIX平台的一个工具，它的作用是将参数列表转换成小块分段传递给其他命令，以避免参数列表过长的问题。如果git branch --merged显示的是a，b，c三个分支已经合并，上面的命令会转换为：git branch -d a b c。更多xargs的信息：http://zh.wikipedia.org/wiki/Xargs