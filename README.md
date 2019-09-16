# 先了解Git、GitHub
> - **git**：团队协作开发中，大部分都会用到版本控制软件，比如Git、Svn等。Git是一个分布式版本控制系统，让程序员团队能够协作开发项目，Git帮助大家管理为项目所做的工作，避免一个人所做的修改影响其他人所做的修改。你在项目中实现一个新功能的时候，Git将跟踪你对每个文件所做的修改。确定代码可行后，你将提交所做的修改，而Git将记录项目最新的状态，如果你犯了错，想撤销所做的修改，可轻松的返回以前的任何可行状态。
> - **GitHub**：是用于版本控制和协作的代码托管平台，它可以让您和其他人在任何地方协同工作。GitHub 可以托管各种Git版本库，并提供一个web界面。GitHub上的项目都存储在仓库中，后者包含与项目相关联的一切：代码，项目参与者的信息，问题和bug报告等。
> **总结**：Github是代码托管平台，是协作的工具;而Git是版本控制工具。Git不需要联网，在本机就可以使用。当然，Git和Github双剑合璧，是最顺畅的。
## Git与GitHub的作用：
![GitHub的分支与合并](https://guides.github.com/activities/hello-world/branching.png)
**简单来说：就是从主分支Master中分出分支Feature,然后再合并merge在一起达成代码迭代更新的过程**
![Github用Git做版本控制](https://pic4.zhimg.com/80/d88e52fc7942ef9a94cc8d957239fc9e_hd.jpg)

![利用Git+Github进行团队协作开发](http://static.open-open.com/lib/uploadImg/20161109/20161109103130_442.png)

***分支的概念***：
- master分支，即主分支。任何项目都必须有个这个分支。对项目进行tag或发布版本等操作，都必须在该分支上进行。
  develop分支，即开发分支，从master分支上检出。团队成员一般不会直接更改该分支，而是分别从该分支检出自己的feature分支，开发完成后将feature分支上的改动merge回develop分支。同时release分支由此分支检出。
 
-  release分支，即发布分支，从develop分支上检出。该分支用作发版前的测试，可进行简单的bug修复。如果bug修复比较复杂，可merge回develop分支后由其他分支进行bug修复。此分支测试完成后，需要同时merge到master和develop分支上。
 
 -  feature分支，即功能分支，从develop分支上检出。团队成员中每个人都维护一个自己的feature分支，并进行开发工作，开发完成后将此分支merge回develop分支。此分支一般用来开发新功能或进行项目维护等。
 
-   fix分支，即补丁分支，由develop分支检出，用作bug修复，bug修复完成需merge回develop分支，并将其删除。所以该分支属于临时性分支。
 
 - hotfix分支，即热补丁分支。和fix分支的区别在于，该分支由master分支检出，进行线上版本的bug修复，修复完成后merge回master分支，并merge到develop分支上，merge完成后也可以将其删除，也属于临时性分支。
 
 ## GitHub网站注册与使用教程
 教程里面，最推荐的是官方的[Hello World](https://guides.github.com/activities/hello-world/)是最权威的
 
 ## Git的本地安装
 Linux系统安装GitHub比较容易，不再这里讨论了
 重点看下怎么在windos系统下安装Git
 ### Git BASH的下载安装
 [Git安装教程（windows）](https://www.cnblogs.com/wj-1314/p/7993819.html)
 [Windows下Git的下载与安装](http://baijiahao.baidu.com/s?id=1601036689157983619&wfr=spider&for=pc)
 #### Git本地配置
 打开Git BASH:
 1. 设置你的用户名和电子邮件
```
git config --global  user.name "Username"
git config --global  user.email "Username@example.com"
```

