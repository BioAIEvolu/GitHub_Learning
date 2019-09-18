# Git与GitHub入门笔记
## 先了解Git、GitHub
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
> 更多：
> 
> [“开发者神器”的GitHub](https://baijiahao.baidu.com/s?id=1594232691312740966&wfr=spider&for=pc)
> 
> [GitHub 官方出了一个交互式教程](https://www.zhihu.com/question/20070065?sort=created)
> 
> [如何正确使用git和github](https://blog.csdn.net/qq_18297675/article/details/79633950)
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

```
$ ssh -T git@github.com
```  

如果是第一次的会提示是否continue，输入yes就会看到：
```
You've successfully authenticated, but GitHub does not provide shell access 
```
这就表示已成功连上github。
2. 设置你的用户名和电子邮件  
github每次commit都会记录他们
```
git config --global  user.name "Username"
git config --global  user.email "Username@example.com"
```
git config命令的--global参数，用了这个参数，表示你这台机器上所有的Git仓库都会使用这个配置，当然也可以对某个仓库指定不同的用户名和Email地址。

### 创建项目

#### 在github网站上创建一个新的repositoy
- 填写项目名称，描述等
- 创建完成后，跳转到下面页面
- 记住这个HTTPS地址
#### 在Git BASH命令行通过mkdir和cd命令，新建并且进入自己的项目文件夹中，然后按顺序输入命令：
- 创建README.md文件  `touch README.md`   
  [标准README.md](http://baijiahao.baidu.com/s?id=1644120438928420577&wfr=spider&for=pc)
- 初始化git仓库  `git init`  
完成初始化后，项目文件夹下多出一个隐藏文件夹.git。

- 将项目的所有文件添加到仓库中 
  ```
  git add .
  ```
  每次增加\、删除和修改文件都需要执行此条命令，然后git stautus看看情况  
  
  将项目中未被跟踪的文件都加入到仓库中，它不提交这些文件，而只是让git开始关注他们。  
  
  如果只想添加某个特定的文件，只需要将.换成特定的名称即可。 
- 提交注释备注
  ```
  git commit -m "有意义的注释语句"
  ```
  拍摄项目的快照。标志-m 让Git接下里的消息（“Started project"）记录到项目中的历史记录中，输出表明我们在分支master 上，而且有一个文件被修改了，可能需要重新配置自己的账号或者名字，再执行上面的代码就会成功  
  
  `-a`参数表示将所有修改了的文件都加入当前提交中。命令`git commit -a `只对状态为M的文件有用，而对新增而为添加的问题是不起作用的，因为我们新添加的文件NewCreateFile仍然处于 Untracked 状态中。 （要先执行`git add .`） 
  
- 关联自己的仓库url地址
  回到刚刚GitHub页面，找到自己的url地址
     
  `git remote add origin https://自己的仓库url地址`     
  与github（远程仓库）建立联系
- 将本地库上传到github服务器上对应的分支中
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

  - 工作目录，持有实际文件 
  - 暂存区，临时保存改动 
  - HEAD，指向最后一次提交的结果  

#### 命令行操作
##### 本地提出更改，添加至暂存区 
```
git add <filename>
git add *
```
##### 将改动实际提交至HEAD
```
git commit -m "代码提交信息"
```
- **二次提交**：
  ```
  git commit -am "备注文字"
  ```
  标志-a 让Git 将仓库中所有修改了的文件都加入当前提交中，（如果我们两次提交之间加入了新文件，我们执行`get add . `操作，将新文件加入到仓库中）标志-m让Git咱提交历史中记录一条消息。
##### 推送改动
你的改动现在已经在本地仓库的 HEAD 中了。执行如下命令以将这些改动提交到远端仓库：
```
$ git push origin (指定分支名称)
```
##### 如果你还没有克隆现有仓库，并欲将你的仓库连接到某个远程服务器，你可以使用如下命令添加：
```
git remote add origin <server>
```
如此你就能够将你的改动推送到所添加的服务器上去了。
##### 克隆
> git clone 是用来从已有的 Git 仓库克隆出一个新的镜像仓库到本地的。
> [有些时候需要带着用户名和密码进行clone](https://www.jianshu.com/p/1cda2620a5ba)
  - 创建**本地仓库**的克隆版本：
    ```
    git clone /path/to/repository
    ```
  - 创建**远端服务器**上的克隆版本：
    ```
    git clone username@host:/path/to/repository
    ```
    该命令会在本地主机生成一个目录，与远程主机的版本库同名。如果要指定不同的目录名，可以将目录名作为`git clone`命令的第二个参数。  
    ```
    $ git clone <版本库的网址> <本地目录名>
    ```
    git clone支持多种协议，除了HTTP(s)以外，还支持SSH、Git、本地文件协议等，下面是一些例子。
    ```
    $ git clone http[s]://example.com/path/to/repo.git/
    $ git clone ssh://example.com/path/to/repo.git/
    $ git clone git://example.com/path/to/repo.git/
    $ git clone /opt/git/project.git 
    $ git clone file:///opt/git/project.git
    $ git clone ftp[s]://example.com/path/to/repo.git/
    $ git clone rsync://example.com/path/to/repo.git/
    ```
    SSH协议还有另一种写法：
    ```
    $ git clone [user@]example.com:path/to/repo.git/
    ```
    通常来说，Git协议下载速度最快，SSH协议用于需要用户认证的场合。各种协议优劣的详细讨论请参考[官方文档](http://git-scm.com/book/en/Git-on-the-Server-The-Protocols)。   
    
    使用https除了速度慢以外，还有个最大的麻烦是每次推送都必须输入口令，但是在某些只开放http端口的公司内部就无法使用ssh协议而只能用https。
    - 克隆一个指定分支到本地
    ```
    git clone -b 分支名 <版本库的网址>
    ```
    更多：
    > [git clone -b 相关](https://www.jianshu.com/p/e1e106467449)
    >
    > [git clone几种可选参数的使用与区别](https://blog.csdn.net/shrimpcolo/article/details/80164741)
    >
    > [git clone 子模块](https://www.jianshu.com/p/0c0ff714bec0)
    >
    > [加快git clone 几十倍速度的小方法 （30KB vs 2M）](https://blog.51cto.com/11887934/2051323)
    > 
    > [Git基本使用方法——clone项目到本地](https://blog.csdn.net/kuuhakuna/article/details/78705778)
##### 分支
分支是用来将特性开发绝缘开来的。在你创建仓库的时候，master 是"默认的"分支。在其他分支上进行开发，完成后再将它们合并到主分支上。
![分支](https://www.runoob.com/wp-content/uploads/2014/05/branches.png)
- **创建一个叫做"feature_x"的分支，并切换过去：**
  ```
  git checkout -b feature_x
  ```
- **切换回主分支：**
  ```
  git checkout master
  ```
- **把新建的分支删掉：**
  ```
  git branch -d feature_x
  ```
- **将分支推送到远端仓库，让其他人可见:**
  ```
  git push origin <branch>
  ```
- 如果文件删除错了，也可以用`git checkout -- 文件名`还原回来。其实就是**用版本库里的版本替换工作区的版本，无论工作区是修改还是删除**。
##### 合并与更新
在分支修改完代码后，就可以合并代码到master上
- **在合并改动之前，你可以使用如下命令预览差异：**
  ```
  git diff <source_branch> <target_branch>
  ```
- **更新你的本地仓库至最新改动(远端服务器-->本地计算机的更新)：**
  多人开发时，在push前一定要先更新本地仓库至最新改动，避免许多不必要的冲突
  ```
  git pull
  ```
  **以在你的工作目录中 *获取（fetch）* 并 *合并（merge）* 远端的改动。**
- **合并其他分支到你的当前分支（例如 master）:(本地计算机)**
  ```
  git merge <branch>
  ```
  
- 在这两种情况下，git 都会尝试去自动合并改动。但可能出现***冲突（conflicts）***。 这时候就需要你修改这些文件来手动合并这些冲突（conflicts）。改完之后，你需要执行如下命令以将它们标记为合并成功：
  ```
  git add <filename>
  ```
  
##### 标签
为软件发布创建标签是推荐的。这个概念早已存在，在 SVN 中也有。你可以执行如下命令创建一个叫做 1.0.0 的标签：
```
git tag 1.0.0 1b2e1d63ff
```
*1b2e1d63ff* 是你想要标记的提交 ID 的前 10 位字符。可以使用下列命令获取提交 ID：
```
git log
```
你也可以使用少一点的提交 ID 前几位，只要它的指向具有唯一性。
##### 替换本地改动
- 假如操作失误，可以使用如下命令替换掉本地改动：
  ```
  git checkout -- <filename>
  ```
  此命令会**使用 HEAD 中的最新内容替换掉你的工作目录中的文件。已添加到暂存区的改动以及新文件都不会受到影响。**    
  
  **注意：**对未暂存的修改文件进行回滚的操作命令生效了，再想找回被丢弃的内容就找不回了，此操作是**不可逆**的
  
- 假如你想丢弃你在本地的所有改动与提交，可以到服务器上获取最新的版本历史，并将你本地主分支指向它：  
  ```
  git fetch origin
  git reset --hard origin/master
  ```
- 另外，对已经暂存的文件执行以下命令，回到了之前暂存的状态。
  ```
  git reset HEAD <文件名> 
  ```
### 更多Git操作命令
- **git rm**：从当前的工作空间中和索引中删除文件，例如'git rm app/model/user.rb'
- **git revert**：如果有远程库存在：使用 `git revert <commit_id>`操作实现**以退为进**， `git revert` 不同于 `git reset` 它不会擦除"回退"之后的 commit_id ,而是正常的当做一次"commit"，产生一次新的操作记录，所以**可以push，不会让你再pull** 。  
> 还原一个版本的修改，必须提供一个具体的Git版本号，例如'git revert bbaf6fb5060b4875b18ff9ff637ce118256d6f20'，Git的版本号都是生成的一个哈希值
- **git config --list**: 查看配置信息
- **git log 文件名**：可以查看该文件所有的修改记录
  - `--pretty=oneline`参数可以简洁的显示`commit`和说明，注意`--pretty=oneline`参数要写在具体文件前。
- **git reset** 命令用于改变版本，
  在Git中，用`HEAD`表示当前版本，上一个版本就是`HEAD^`，上上一个版本就是`HEAD^^`，当然往上100个版本写100个^比较容易数不过来，所以写成`HEAD~100`。
  - **回滚到上一个版本**
    ```
    git reset --hard HEAD^
    ```
  - **想回到最新的版本，取消这次回滚**
    ```
    git reset  --hard  "commit  id"
    ```
    这样就可以去到指定commit id的版本。

    版本号没必要写全，前几位就可以了，Git会自动去找，只要保证id唯一就行。
- **git reflog**:如果找不到已经删除版本的commit id的话，可以用git reflog显示所有版本的commit 记录。git  log不能查看已经删除的commit，但是git reflog可以。

##### [Git远程操作命令](http://www.ruanyifeng.com/blog/2014/06/git_remote.html)
![Git远程操作](http://www.ruanyifeng.com/blogimg/asset/2014/bg2014061202.jpg)
- git clone
- git remote
- git fetch
- git pull
- git push
###### Git Remote
本地是配了github的ssh-key的，所以也是支持ssh的链接的。下方我们将根据 git remote 远程仓库操作来添加上ssh的仓库地址。  
   
**查看和修改远端地址**  

为了便于管理，Git要求每个远程主机都必须指定一个主机名。`git remote`命令就用于管理主机名。 
- 不带选项的时候，`git remote`命令列出所有远程主机。  
  ```
  $ git remote
  origin
  ```
- 使用`-v`选项，可以参看远程主机的网址。
  ```
  $ git remote
  origin  https://github.com/BioAIEvolu/GitHub_Learning.git (fetch)
  origin  https://github.com/BioAIEvolu/GitHub_Learning.git (push)
  ```
  上面命令表示，当前只有一台远程主机，叫做origin，以及它的网址。  
  
- 克隆版本库的时候，所使用的远程主机自动被Git命名为origin。如果想用其他的主机名，需要用git clone命令的-o选项指定。
  ```
  $ git clone -o jQuery https://github.com/jquery/jquery.git
  $ git remote
  jQuery
  ```
  上面命令表示，克隆的时候，指定远程主机叫做jQuery。
- `git remote show`命令加上主机名，可以查看该主机的详细信息。
  ```
  $ git remote show origin
  ```
- `git remote add`命令用于添加远程主机。
  ```
  $ git remote add <主机名> <网址>
  ```
- `git remote rm`命令用于删除远程主机。
  ```
  $ git remote rm <主机名>
  ```
- `git remote rename`命令用于远程主机的改名。
  ```
  $ git remote rename <原主机名> <新主机名>
  ```
###### git fetch

- 一旦远程主机的版本库有了更新（Git术语叫做commit），需要将这些更新取回本地，这时就要用到`git fetch`命令。
  ```
  $ git fetch <远程主机名>
  ```
  上面命令将某个远程主机的更新，全部取回本地。    

  git fetch命令通常用来查看其他人的进程，因为它取回的代码对你本地的开发代码没有影响。  

  默认情况下，git fetch取回所有分支（branch）的更新。如果只想取回特定分支的更新，可以指定分支名。  
  ```
  $ git fetch <远程主机名> <分支名>
  ```
  比如，取回origin主机的master分支。
  ```
  $ git fetch origin master
  ```
  所取回的更新，在本地主机上要用"远程主机名/分支名"的形式读取。比如`origin`主机的`master`，就要用`origin/master`读取。  

- `git branch`命令的`-r`选项，可以用来查看远程分支，`-a`选项查看所有分支
  ```
  $ git branch -r
    origin/master
  ```
  ```
  $ git branch -a
    feature
  * master
    remotes/origin/master
  ```
  上面命令表示，本地主机的当前分支是master，远程分支是origin/master。  

  取回远程主机的更新以后，可以在它的基础上，使用`git checkout`命令创建一个新的分支。
  ```
  $ git checkout -b newBrach origin/master
  ```
  上面命令表示，在`origin/master`的基础上，创建一个新分支。  
  
- 此外，也可以使用`git merge`命令或者`git rebase`命令，在本地分支上合并远程分支。
    ```
    $ git merge origin/master
    # 或者
    $ git rebase origin/master
    ```
    面命令表示在当前分支上，合并`origin/master`
###### git pull
- `git pull`命令的作用是，取回远程主机某个分支的更新，再与本地的指定分支合并。它的完整格式稍稍有点复杂。
  ```
  $ git pull <远程主机名> <远程分支名>:<本地分支名>
  ```
  比如，取回`origin`主机的`next`分支，与本地的`master`分支合并，需要写成下面这样。
  ```
  $ git pull origin next:master
  ```
  如果远程分支是与当前分支合并，则冒号后面的部分可以省略。
  ```
  $ git pull origin next
  ```
  上面命令表示，取回origin/next分支，再与当前分支合并。实质上，这等同于先做`git fetch`，再做`git merge`。
  ```
  $ git fetch origin
  $ git merge origin/next
  ```
  在某些场合，Git会自动在本地分支与远程分支之间，建立一种**追踪关系（tracking）**。比如，在`git clone`的时候，所有本地分支默认与远程主机的同名分支，建立追踪关系，也就是说，本地的`master`分支自动"追踪"`origin/master`分支。  
  
  Git也允许手动建立追踪关系。
  ```
  git branch --set-upstream master origin/next
  ```
  上面命令指定`master`分支追踪`origin/nex`t分支。   
  
  如果当前分支与远程分支存在追踪关系，`git pull`就可以省略远程分支名。  
  ```
  $ git pull origin
  ```
  上面命令表示，本地的当前分支自动与对应的`origin`主机"追踪分支"（remote-tracking branch）进行合并。  

  如果当前分支只有一个追踪分支，连远程主机名都可以省略。
  ```
  $ git pull
  ```
  上面命令表示，当前分支自动与唯一一个追踪分支进行合并。
  
  如果合并需要采用`rebase`模式，可以使用`--rebase`选项。
  ```
  $ git pull --rebase <远程主机名> <远程分支名>:<本地分支名>
  ```
  如果远程主机删除了某个分支，默认情况下，`git pull`不会在拉取远程分支的时候，删除对应的本地分支。这是为了防止，由于其他人操作了远程主机，导致`git pull`不知不觉删除了本地分支。  
  
  但是，你可以改变这个行为，加上参数 `-p `就会在本地删除远程已经删除的分支。
  ```
  $ git pull -p
  # 等同于下面的命令
  $ git fetch --prune origin 
  $ git fetch -p
  ```
###### git push
- `git push`命令用于将本地分支的更新，推送到远程主机。它的格式与`git pull`命令相仿。
  ```
  $ git push <远程主机名> <本地分支名>:<远程分支名>
  ```
  注意，分支推送顺序的写法是<来源地>:<目的地>，所以`git pull`是<远程分支>:<本地分支>，而`git push`是<本地分支>:<远程分支>。  
  
- 如果省略远程分支名，则表示将本地分支推送与之存在"追踪关系"的远程分支（通常两者同名），如果该远程分支不存在，则会被新建。
  ```
  $ git push origin master
  ```
  上面命令表示，将本地的`master`分支推送到`origin`主机的`master`分支。如果后者不存在，则会被新建。  
    
- 如果省略本地分支名，则表示删除指定的远程分支，因为这等同于推送一个空的本地分支到远程分支。
  ```
  $ git push origin :master
  # 等同于
  $ git push origin --delete master
  ```
  上面命令表示删除`origin`主机的`master`分支。  
  
- 如果当前分支与远程分支之间存在追踪关系，则本地分支和远程分支都可以省略。
  ```
  $ git push origin
  ```
  上面命令表示，将当前分支推送到origin主机的对应分支。  
  
  如果当前分支只有一个追踪分支，那么主机名都可以省略。
  ```
  $ git push
  ```
- 如果当前分支与多个主机存在追踪关系，则可以使用`-u`选项指定一个默认主机，这样后面就可以不加任何参数使用`git push`
  ```
  $ git push -u origin master
  ```
  上面命令将本地的`master`分支推送到`origin`主机，同时指定`origin`为默认主机，后面就可以不加任何参数使用`git push`了。  

- 不带任何参数的`git push`，默认只推送当前分支，这叫做**simple方式**。此外，还有一种**matching方式**，会推送所有有对应的远程分支的本地分支。Git 2.0版本之前，默认采用`matching`方法，现在改为默认采用`simple`方式。如果要修改这个设置，可以采用`git config`命令。
  ```
  $ git config --global push.default matching
  # 或者
  $ git config --global push.default simple
  ```
- 还有一种情况，就是不管是否存在对应的远程分支，将本地的所有分支都推送到远程主机，这时需要使用`--all`选项。
  ```
  $ git push --all origin
  ```
  上面命令表示，将所有本地分支都推送到`origin`主机。  
  
  如果远程主机的版本比本地版本更新，推送时Git会报错，要求先在本地做`git pull`合并差异，然后再推送到远程主机。这时，如果你一定要推送，可以使用`--force`选项。
  ```
  $ git push --force origin 
  ```
  上面命令使用`--force`选项，结果导致远程主机上更新的版本被覆盖。除非你很确定要这样做，否则应该尽量避免使用`--force`选项。
- 最后，`git push`不会推送标签（**tag**），除非使用`--tags`选项。
  ```
  $ git push origin --tags
  ```
#### git命令总结
![git命令总结](https://upload-images.jianshu.io/upload_images/2514846-3ee74d5df5c078f1.png?imageMogr2/auto-orient/strip|imageView2/2/w/608/format/webp)
![git技术栈](https://i.loli.net/2019/09/19/l3pAXzs1Iqd9vZW.png)
### 参考文献
- [Github 简明教程](https://www.runoob.com/w3cnote/git-guide.html)
- [git各种命令介绍以及碰到的各种坑](https://www.cnblogs.com/smiler/p/5074124.html)
- [Git知识总览(一) 从 git clone 和 git status 谈起](https://www.cnblogs.com/ludashi/p/8052739.html)
- [git命令之git clone用法](https://blog.csdn.net/qq_42672770/article/details/81317778)
- [GitFlow工作流：Git+Github团队协作开发](https://www.cnblogs.com/yhaing/p/8473746.html) **推荐**
- [记录自己使用GitHub的点点滴滴](https://www.cnblogs.com/wj-1314/p/9901763.html)
- [浅谈使用git进行版本控制](https://www.cnblogs.com/wj-1314/p/7992543.html)  **这个博客对git版本控制描述不错，推荐看**
- [git之一： 在windows下安装git和使用总结](https://www.cnblogs.com/sunny18/p/8831939.html) 
- [Git远程操作详解](http://www.ruanyifeng.com/blog/2014/06/git_remote.html)
- [【图文详解】如何利用Github在Markdown中插入图片？](https://www.jianshu.com/p/c7618a53454f) 
- [Markdown中插入图片有什么技巧？](https://www.zhihu.com/question/21065229)

