# 先了解Git、GitHub
> - **git**：团队协作开发中，大部分都会用到版本控制软件，比如Git、Svn等。Git是一个分布式版本控制系统，让程序员团队能够协作开发项目，Git帮助大家管理为项目所做的工作，避免一个人所做的修改影响其他人所做的修改。你在项目中实现一个新功能的时候，Git将跟踪你对每个文件所做的修改。确定代码可行后，你将提交所做的修改，而Git将记录项目最新的状态，如果你犯了错，想撤销所做的修改，可轻松的返回以前的任何可行状态。
> - **GitHub**：是用于版本控制和协作的代码托管平台，它可以让您和其他人在任何地方协同工作。GitHub 可以托管各种Git版本库，并提供一个web界面。GitHub上的项目都存储在仓库中，后者包含与项目相关联的一切：代码，项目参与者的信息，问题和bug报告等。
> **总结**：Github是代码托管平台，是协作的工具;而Git是版本控制工具。Git不需要联网，在本机就可以使用。当然，Git和Github双剑合璧，是最顺畅的。
## Git与GitHub的作用：
![GitHub的分支与合并](https://guides.github.com/activities/hello-world/branching.png)
**简单来说：就是从主分支Master中分出分支Feature,然后再合并merge在一起达成代码迭代更新的过程**
![Github用Git做版本控制](https://pic4.zhimg.com/80/d88e52fc7942ef9a94cc8d957239fc9e_hd.jpg)

![利用Git+Github进行团队协作开发](http://static.open-open.com/lib/uploadImg/20161109/20161109103130_442.png)
***一些 GitHub 的基本概念**：
- Repository
仓库的意思，即你的项目，你想在 GitHub 上开源一个项目，那就必须要新建一个 Repository ，如果你开源的项目多了，你就拥有了多个 Repositories 。

- Issue
问题的意思，举个例子，就是你开源了一个项目，别人发现你的项目中有bug，或者哪些地方做的不够好，他就可以给你提个 Issue ，即问题，提的问题多了，也就是 Issues ，然后你看到了这些问题就可以去逐个修复，修复ok了就可以一个个的 Close 掉。

- Star
这个好理解，就是给项目点赞，但是在 GitHub 上的点赞远比微博、知乎点赞难的多，如果你有一个项目获得100个star都算很不容易了！

- Fork
这个不好翻译，如果实在要翻译我把他翻译成分叉，什么意思呢？你开源了一个项目，别人想在你这个项目的基础上做些改进，然后应用到自己的项目中，这个时候他就可以 Fork 你的项目，这个时候他的 GitHub 主页上就多了一个项目，只不过这个项目是基于你的项目基础（本质上是在原有项目的基础上新建了一个分支，分支的概念后面会在讲解Git的时候说到），他就可以随心所欲的去改进，但是丝毫不会影响原有项目的代码与结构。

- Pull Request
发起请求，这个其实是基于 Fork 的，还是上面那个例子，如果别人在你基础上做了改进，后来觉得改进的很不错，应该要把这些改进让更多的人收益，于是就想把自己的改进合并到原有项目里，这个时候他就可以发起一个 Pull Request（简称PR） ，原有项目创建人就可以收到这个请求，这个时候他会仔细review你的代码，并且测试觉得OK了，就会接受你的PR，这个时候你做的改进原有项目就会拥有了。

- Watch
这个也好理解就是观察，如果你 Watch 了某个项目，那么以后只要这个项目有任何更新，你都会第一时间收到关于这个项目的通知提醒。

- Gist
有些时候你没有项目可以开源，只是单纯的想分享一些代码片段，那这个时候 Gist 就派上用场了！  

***分支的概念***：
- master分支，即主分支。任何项目都必须有个这个分支。对项目进行tag或发布版本等操作，都必须在该分支上进行。
  develop分支，即开发分支，从master分支上检出。团队成员一般不会直接更改该分支，而是分别从该分支检出自己的feature分支，开发完成后将feature分支上的改动merge回develop分支。同时release分支由此分支检出。
 
-  release分支，即发布分支，从develop分支上检出。该分支用作发版前的测试，可进行简单的bug修复。如果bug修复比较复杂，可merge回develop分支后由其他分支进行bug修复。此分支测试完成后，需要同时merge到master和develop分支上。
 
 -  feature分支，即功能分支，从develop分支上检出。团队成员中每个人都维护一个自己的feature分支，并进行开发工作，开发完成后将此分支merge回develop分支。此分支一般用来开发新功能或进行项目维护等。
 
-   fix分支，即补丁分支，由develop分支检出，用作bug修复，bug修复完成需merge回develop分支，并将其删除。所以该分支属于临时性分支。
 
 - hotfix分支，即热补丁分支。和fix分支的区别在于，该分支由master分支检出，进行线上版本的bug修复，修复完成后merge回master分支，并merge到develop分支上，merge完成后也可以将其删除，也属于临时性分支。
 
 ## GitHub网站注册与使用教程
 教程里面，最推荐的是官方的[Hello World](https://guides.github.com/activities/hello-world/)是最权威的
 
 ## Git的本地安装与使用
 Linux系统安装GitHub比较容易，不再这里讨论了
 重点看下怎么在windos系统下安装Git
 ### Git BASH的下载安装
 [Git安装教程（windows）](https://www.cnblogs.com/wj-1314/p/7993819.html)
 [Windows下Git的下载与安装](http://baijiahao.baidu.com/s?id=1601036689157983619&wfr=spider&for=pc)
 ### Git命令行的使用
 git在本地git中的使用其实跟在GitHub网页上操作的步骤对的一样的  
 #### Git本地配置
 打开Git BASH:
1. 首先在本地创建ssh key；
`$ ssh-keygen -t rsa -C "your_email@youremail.com"`
- 后面的your_email@youremail.com改为你在github上注册的邮箱，之后会要求确认路径和输入密码，我们这使用默认的一路回车就行。成功的话会在~/下生成.ssh文件夹，进去，打开id_rsa.pub，复制里面的key。
- 回到github上，进入 Account Settings（账户配置），左边选择SSH Keys，Add SSH Key,title随便填，粘贴在你电脑上生成的key。
![输入key](https://www.runoob.com/wp-content/uploads/2014/05/github-account.jpg)
- 为了验证是否成功，在git bash下输入：
`$ ssh -T git@github.com`
如果是第一次的会提示是否continue，输入yes就会看到：You've successfully authenticated, but GitHub does not provide shell access 。这就表示已成功连上github。
2. 设置你的用户名和电子邮件  
github每次commit都会记录他们
```
git config --global  user.name "Username"
git config --global  user.email "Username@example.com"
```
git config命令的--global参数，用了这个参数，表示你这台机器上所有的Git仓库都会使用这个配置，当然也可以对某个仓库指定不同的用户名和Email地址。

### 创建项目

#### 在github网站上创建一个新的repositoy
填写项目名称，描述等
![创建一个新的repositoy](https://img2018.cnblogs.com/blog/1226410/201811/1226410-20181105112500442-122748843.png)
创建完成后，跳转到下面页面
[跳转页](https://img2018.cnblogs.com/blog/1226410/201811/1226410-20181105112652691-726837378.png)
记住这个HTTPS地址
#### 在Git BASH命令行通过mkdir和cd命令，新建并且进入自己的项目文件夹中，然后按顺序输入命令：
- 创建README.md文件  `touch README.md`   
  [标准README.md](http://baijiahao.baidu.com/s?id=1644120438928420577&wfr=spider&for=pc)
- 初始化git仓库  `git init`  
完成初始化后，项目文件夹下多出一个隐藏文件夹.git。

- 将项目的所有文件添加到仓库中 `git add .`    
将项目中未被跟踪的文件都加入到仓库中，它不提交这些文件，而只是让git开始关注他们。  
如果只想添加某个特定的文件，只需要将.换成特定的名称即可。 
- 提交注释备注
`git commit -m "有意义的注释语句"`  
拍摄项目的快照。标志-m 让Git接下里的消息（“Started project"）记录到项目中的历史记录中，输出表明我们在分支master 上，而且有一个文件被修改了，可能需要重新配置自己的账号或者名字，再执行上面的代码就会成功
  
- 关联自己的仓库url地址
回到刚刚GitHub页面，找到自己的url地址
     
`git remote add origin https://自己的仓库url地址`     
与github（远程仓库）建立联系
- 将本地库上传到github上
`git push -u origin master`   
  执行完毕后，如果没有异常，会等待几秒，然后跳出一个让我们输入Username 和password的窗口，我们只需要输入个人的github登录账号和密码即可。  
  
  把本地库study的所有内容推送到远程仓库（也就是Github）上，此后，每次本地提交后，只要有必要，就可以使用命令`git push origin master`推送最新修改；    
  
  至此就完成了将本地项目上传到Github的整个过程。(PS:加入创建的项目文件夹里面含有VScode中项目的Python代码，则VScode的整个就被上传到GitHub了)  
- 检查状态 `git status`  
检查日志和分支信息  
- 查看提交历史 `git log`  
每次提交的时候，Git都会生成一个包含40字符的独一无二的引用ID，它记录提交是谁执行的，提交的时间以及提交的指定消息，并非在任何情况下你都需要所有的这些信息，因此Git提供一个选项，让我们能够打印提交历史条目的更简单的版本。
```
$ git log --pretty=oneline
5d6cecad80427924b94b14c6fd2bb82a4fa86840 (HEAD -> master) Started project
```   
标志 --pretty=oneline   指定显示一项最重要的信息，提交的引用ID以及为提交记录的消息。

### 删除项目

在GitHub -->点入需要删除项目 -->点开setting -->将滚动条滑到底部，找到Danger Zone下的Delete this repository -->点击，会弹出一个警告框，将该项目名称输入进行确认 -->输入密码确认 -->删除成功后，会重新回到个人主界面提醒项目删除成功

### 工作流程
![三棵树](https://www.runoob.com/wp-content/uploads/2014/05/trees.png)
Git本地仓库实际上由三个tree组成
- 1.工作目录，持有实际文件 
- 2. 暂存区，临时保存改动 
- 3. HEAD，指向最后一次提交的结果
#### 命令行操作
- 本地提出更改，添加至暂存区 
```
git add <filename>
git add *
```
- 将改动实际提交至HEAD
```
git commit -m "代码提交信息"
```
- 推送改动
你的改动现在已经在本地仓库的 HEAD 中了。执行如下命令以将这些改动提交到远端仓库：
```
$ git push origin (指定分支名称)
```
如果你还没有克隆现有仓库，并欲将你的仓库连接到某个远程服务器，你可以使用如下命令添加：
```
git remote add origin <server>
```
如此你就能够将你的改动推送到所添加的服务器上去了。
- 克隆
  - 创建**本地仓库**的克隆版本：
    ```
    git clone /path/to/repository
    ```
  - 创建**远端服务器**上的克隆版本：
    ```
    git clone username@host:/path/to/repository
    ```

