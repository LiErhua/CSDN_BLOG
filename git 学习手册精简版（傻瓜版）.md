# git 学习手册精简版（傻瓜版）不断更新

作者：李二花

## 基本操作

第一步：首先要进入GitHub注册一下，并记住自己的用户名，邮箱和密码

第二步：找一个空白的文件夹，打开命令行窗口cd 到此目录下（具体的操作方法见http://blog.csdn.net/cdqn10086/article/details/53978825）

进行自报家门的操作

```git
git config --global user.name YourName
git config --global user.email YourEmail
```

建立要进行版本控制的操作（建立一个文件夹，一切操作在其中进行）

```git
mkdir demo01 %建立文件夹名字为demo01
cd demo01   %进入此文件夹
git init    %进行init，将这个目录变成git管理的仓库
进行完此项之后，会在demo01文件夹内有一个.git文件，要用ls -ah来查看隐藏文件。
```

对里面的文件进行操作（新建一个文本文档demo01.txt，并输入几句英文）

```git
git add demo01.txt
git commit -m "this is the first demo"
```

## 远程仓库（GitHub）

第一步：获取SSH（打开命令行，进行如下操作）

```
$ ssh-keygen -t rsa -C YourEmail
```

进行此命令之后，我们就可以找到文件夹.ssh ，因为.ssh文件件在主目录下，因此可以直接如下方式打开

```cmd
$ open ~/.ssh
```

第二步：找到我们需要的两个文件，id_rsa （私人秘钥，万勿泄露）和id_rsa.pub（公钥），然后登陆GitHub，找到Account settings中的SSH Keys，新建sshkey，title写一个平时常用的名字即可，key里面输入我们公钥里的所有的内容。

第三步：在GitHub的个人页处新添加一个仓库(我们新建的仓库名字就是demo01)

**本地库关联远程库**

第四步：为了让本地的与远程的同步，我们在本地的demo01仓库下运行如下的命令

```cmd
git init #初始化，如果上一步完成了这一步就不用了
git remote add origin https://github.com/用户名/demo01.git (此时我们的远程库就叫做名字origin)
```

使用如下将本地库推送到远程库

```cmd
git push -u origin master				
```

现在也就是完成了本地库的提交，以后，只要是有了新的改动，本地做了提交，都可以通过如下命令来进行把本地的master分支推送到GitHub。

```cmd
git push origin master
```

**远程库克隆到本地**

首先，要在GitHub上建立一个远程仓库并且生成readme.txt文件

然后，在选择你要保存的一个目录，在此目录下进行如下克隆

```cmd
git clone https://github.com/LiErhua（GitHub用户名）/demo02.git
```

然后会发现已经克隆到自己的硬盘本地了。

**notice：**

其中我们push和clone时，地址都是有两种选择的，一种是SSH，一种是http协议的分别如下

```http
git@github.com:你的GitHub用户名/文件夹名称.git
https://github.com/用户名/文件夹名称.git
```



