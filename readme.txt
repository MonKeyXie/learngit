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

时光穿梭机：
