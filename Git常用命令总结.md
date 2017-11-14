---
title: Git常用命令总结
date: 2017-09-29 21:50:46
tags: Git
categories: Git 
---

* 配置用户名密码

    git config --global user.name ""
  
    git config --global user.email ""
  
* 保存内容到暂存区

    git add 保存文件名称
  
    git add .(保存全部文件)
  
* 提交

    git commit -m "提交的说明"

* 新建并切换分支
     
    git checkout -b 分支名
  
* 提交内容到对应分支

    git push origin 分支名
    
    git push -u origin 分支名(首次提交)

* 连接远程仓库

    git remote add origin 远程仓库地址
  
* 查看所有分支

     git branch
  
* 切换分支

    git checkout 分支名
  
* 克隆代码
 
    git clone 远程仓库地址

* 获取远程分支

    git pull origin 远程分支名：本地分支名 将远程分支获取下来并合并本地分支
        
    相当于git fetch加git merge

* 查看当前用户名和邮箱

    git config user.name    查看用户名

    git config user.email    查看邮箱

* 查看日志文件

    git log