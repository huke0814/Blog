---
title: Git教程
toc: true
mathjax: true
date: 2019-09-22 22:06:55
author: huke8
img:
top: true
cover: true
coverlmg:
password:
summary: 关于git的简单操作
tags: 随记
categories: software language
---

# 一、创建版本库

- 首先需要在合适的地方创建一个空目录：打开`Git Bash`，`cd`到要创建目录的路径，执行以下命令。

  ```git
  $ mkdir 目录名字
  $ cd 目录名字
  $ pwd
  /Users/michael/目录名字
  ```

  `pwd`命令用于显示当前路径。切记各个目录名字都不要包含中文。

- 再把这个目录变成版本库

  ```git
  $ git init
  Initialized empty Git repository in /Users/michael/目录名字/.git/
  ```

  这样一个空的版本库就创建完成了。

  下次要进入这个仓库时，先打开仓库的目录，在该目录下，右键选择`Git Bash Here`，就可以操作这个仓库了。

# 二、把文件添加到版本库

- 使用`vi`命令进入`readme.txt`文件，如果文件不存在将会创建。

  ```git
  $ vi readme.txt
  ```

  这时界面进入到`readme.txt`文件中。

  输入命令`a`后，就可以编辑文件了。（命令显示在窗口的最下面）

  编辑完成后，按`Esc`键退出编辑，再输入命令`: wq`即可退出文件(或者大写`ZZ`即按住`shift`+`zz`)。

- 把文件添加到仓库中。

  ```git
  $ git add readme.txt
  ```

  执行上面的命令，没有任何显示则说明添加成功了。

- 再把文件提交到仓库中。

  ```git
  $ git commit -m "wrote a readme file"
  [master (root-commit) eaadf4e] wrote a readme file
   1 file changed, 2 insertions(+)
   create mode 100644 readme.txt
  ```

  `-m`后面输入的是本次提交的说明，可以输入任意内容，当然最好是有意义的，这样你就能从历史记录里方便地找到改动记录。

- 可以看出，添加文件到Git仓库，分两步：

  1. 使用命令`git add <file>`，注意，可反复多次使用，添加多个文件；
  2. 使用命令`git commit -m <message>`，完成。

# 三、时光穿梭

> 记录你修改文件的历史

### 1、修改文件

- 按照之前讲解的编辑`readme.txt`文件的步骤，对文件进行修改。

- 运行`git status`命令可以看结果：

  ```git
  $ git status
  On branch master
  Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git checkout -- <file>..." to discard changes in working directory)
  
  	modified:   readme.txt
  
  no changes added to commit (use "git add" and/or "git commit -a")
  ```

  只告诉了我们`readme.txt`被修改过了，但是还没有被提交。

- 运行`git diff`命令可以看到具体修改了什么：

  ```git
  $ git diff readme.txt 
  diff --git a/readme.txt b/readme.txt
  index 46d49bf..9247db6 100644
  --- a/readme.txt
  +++ b/readme.txt
  @@ -1,2 +1,2 @@
  -Git is a version control system.
  +Git is a distributed version control system.
   Git is free software.
  ```

  `-`和`+`分别对应着修改前和修改后的内容，一目了然。

- 最后再运行`git add <file>`和`git commit -m <message>`命令，把你修改后的文件添加并提交到仓库中。

  注意：任何时候你都可以运行`git status`命令来查看当前的状态，如果`git status`告诉你有文件被修改过，则可以用`git diff`查看修改内容。

### 2、版本退回