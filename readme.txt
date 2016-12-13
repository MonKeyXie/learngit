Git is a distributed version control system.
Git is a free software distributed under the GPL.
Git has a mutable index called stage
Git tracks changes.
Creating a new branch is quick and simple..
This is a small change

创建版本库：
第一步，创建版本库-选择合适的地方，创建空目录：
$ mkdir learngit
$ cd learngit
$ pwd		--pwd命令用于显示当前目录（路径）。
注：windows下不要用中文命名仓库

第二步，通过git init命令把这个目录变成Git可以管理的仓库：

$ git init	--让repository真正可以使用

注：windows下不要用记事本编辑.txt

第三步，把文件添加到repository
1.把想上传的文件放到仓库(如：learngit文件夹)目录下
2.$ git add readme.txt
3.git commit告诉Git，把文件提交到仓库：
  eg:$ git commit -m "wrote a readme file"
  -m后面输入的是本次提交的说明.

时光穿梭机(修改)：
git status命令可以让我们时刻掌握仓库当前的状态
git diff这个命令来查看具体修改，若已经记不清上次怎么修改的readme.txt
提交修改也是git add ，git commit -m "修改信息"

版本回退：
git log命令显示你所有提交的记录(里面有每个版本的commit id)
git log --pretty=oneline是上面的简约版
git reset命令把当前版本b回退到上一个版本a
git reset --hard HEAD^ 上一个版本就是HEAD^，上上一个版本就是HEAD^^，当然往上100个版本写100个^比较容易数不过来，所以写成HEAD~100

取消回退：
若退回后后悔了，只要上面的命令行窗口还没有被关掉，你就可以顺着往上找啊找啊，找到那个b版本的commit id是3628164...，于是就可以指定回到未来的某个版本：
$ git reset --hard 3628164 版本号没必要写全，前几位就可以了，Git会自动去找。

git reflog用来记录你的每一次命令，命令行关了输入这个，就可以找到版本b的commit id了

工作区和暂存区；
可更改文件是工作区里的，如.txt文件
版本库包括 暂存区 和 分支master已经HEAD
git add时把修改加到缓存区(stage)，git commit时把stage里的内容提交到当前branch

管理修改：
Git比其他版本控制系统设计得优秀，因为Git跟踪并管理的是修改，而非文件。

撤销修改：
还没git add到缓存区：git checkout -- file，可以丢弃工作区的修改
已经git add到缓存区：git reset HEAD file可以把暂存区的修改撤销掉（unstage），重新放回工作区，再git checkout --file

删除文件：
确实要从版本库中删除该文件，那就用命令git rm file删掉，并且git commit
另一种情况是删错了，因为版本库里还有呢，所以可以很轻松地把误删的文件恢复到最新版本：
$ git checkout -- test.txt
git checkout其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”。

添加远程库：
Create a new repo”按钮，创建一个新的仓库。
Repository name填入learngit，其他保持默认设置，点击“Create repository”按钮，就成功地创建了一个新的Git仓库
在本地的learngit仓库下运行命令：
$ git remote add origin git@github.com:MonKeyXie/learngit.git
添加后，远程库的名字就是origin，这是Git默认的叫法，也可以改成别的，但是origin这个名字一看就知道是远程库。

推送当前分支：
由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。
$ git push -u origin master	第一次推送
$ git push origin master	往后推送

clone远程库：
创建一个新的仓库，名字叫gitskills，我们勾选Initialize this repository with a README，这样GitHub会自动为我们创建一个README.md文件。
接下来用命令git clone克隆一个本地库：
$ git clone git@github.com:MonKeyXie/gitskills.git
还可以用https://github.com/MonKeyXie/gitskills.git这样的地址。实际上，Git支持多种协议，默认的git://使用ssh，但也可以使用https等其他协议。

