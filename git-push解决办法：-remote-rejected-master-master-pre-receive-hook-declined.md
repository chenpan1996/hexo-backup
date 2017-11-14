---
title: 'git push解决办法： ! [remote rejected] master -> master (pre-receive hook declined)'
date: 2017-09-29 22:10:56
tags: Git
categories: Git 
---
前天准备上传一个project到GitLab上，但是试了很多次都上传不上去，报错如下：

 ! [remote rejected] master -> master (pre-receive hook declined)

截图：

 ![](http://i.imgur.com/YCD9tA2.png)

一开始还以为自己用户名和密码错误，试了好多次，网上搜所索也没搜索到明确的结果，不过最后还是找到了解决的办法。

git push不上去的原因在于所push的分支权限为protected,只有项目的管理员或者项目的管理员指派的具有相应权限的人才能进行push,要进行项目的push,有如下两种方法：

### 1.将所要push的内容所在的分支的protected权限关闭


(1)进入所在项目的settings

![](http://i.imgur.com/F8Lgf37.png)

(2)点击进入Protected branches,点击unprotected将master分支的权限改变，即关闭master的protected权限

![](http://i.imgur.com/aLQQpJn.png)


### 2.新建其它分支，将项目push到新建的分支上，后期再进行merge

(1)新建分支

    git branch 分支名

(2)切换分支

    git checkout 分支名

(3)进行项目上传

    git add .
   
    git commit -m "提交的信息"

    git remote add origin 远程仓库地址

    git push -u origin 分支名