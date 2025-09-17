---
date: 2025-09-17
tags:
  - 计算机科学
  - 开发相关
  - 开发学习
  - Git
aliases:
---
## Git相关简介，诞生，集中式分布式
略

## 基本指令
##### git init
在选好的本地文件夹输入这个命令，可以在那里建立一个git仓库
##### git add
告诉git，准备把文件添加到仓库
##### git commit -m
写了啥功能什么的，后面备注一下
##### git remote add origin 你的仓库链接
关联你的仓库，一般origin是默认名字，一看就知道是远程仓库
##### git push origin master
推送你master分支上的内容过去，第一次要输入git push -u origin master
加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令
就是说当你第一次用了-u参数后，本地和远程会创建同名分支（如master）,本地的master和远程origin的master分支关联起来。以后直接`git push`即可，此时`git push`就相当于`git push origin master`了

## 其他常用命令

##### git log
`git log`命令显示从最近到最远的提交日志，我们可以看到3次提交，最近的一次是`append GPL`，上一次是`add distributed`，最早的一次是`wrote a readme file`。

用`HEAD`表示当前版本，上一个版本就是`HEAD^`，上上一个版本就是`HEAD^^`，往上100个版本写成`HEAD~100`。
##### git reset --hard HEAD^
`--hard`会回退到上个版本的已提交状态，而`--soft`会回退到上个版本的未提交状态，`--mixed`会回退到上个版本已添加但未提交的状态。
##### git reset --hard 版本号
可以重返未来
##### git reflog
可以查看到你的每一次命令，以便确定你去哪个版本

##### git clone
git clone git@github.com：id/仓库名.git
克隆一份到本地仓库

## 工作区和暂存区，管理修改
待学习，打算在我之后做项目有这个需求的时候再学习，目前只学习以上基本用法
