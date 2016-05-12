this is a version git
demand:git init ,git add <file>,git status,git diff,git commit -m "****",
further demand:git log (查看修改日志)，or git log --pretty=oneline(一行显示)
				git reset --hard HEAD^（回退到上一个版本）or  git reset --HEAD~100(回退到上100个版本)，git reset --hard 3628164（回到指定版本号的版本，maybe newer older）
				要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本
				用git diff HEAD -- readme.txt命令可以查看工作区和版本库里面最新版本的区别
				你可以发现，Git会告诉你，git checkout -- file可以丢弃工作区的修改
				命令git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：

一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态

Git同样告诉我们，用命令git reset HEAD file可以把暂存区的修改撤销掉（unstage），重新放回工作区


删除文件：工作区，直接rm，一是确实要从版本库中删除该文件，那就用命令git rm删掉，并且git commit

创建Hubgit 链接
$ ssh-keygen -t rsa -C "hxm_at1991@163.com"

Your identification has been saved in /c/Users/hxm/.ssh/id_rsa.
Your public key has been saved in /c/Users/hxm/.ssh/id_rsa.pub.

要关联一个远程库，使用命令git remote add origin git@server-name:path/repo-name.git；
git remote add origin https://github.com/BurningAbys2/learngit.git

关联后，使用命令git push -u origin master第一次推送master分支的所有内容；

此后，每次本地提交后，只要有必要，就可以使用命令git push origin master推送最新修改

 从远程库clone版本：git clone git@github.com:BuringAbys2/gitskills.git
 
 
 Git鼓励大量使用分支：

查看分支：git branch

创建分支：git branch <name>

切换分支：git checkout <name>

创建+切换分支：git checkout -b <name>

合并某分支到当前分支：git merge <name>

删除分支：git branch -d <name>

小结

在GitHub上，可以任意Fork开源仓库；

自己拥有Fork后的仓库的读写权限；

可以推送pull request给官方仓库来贡献代码。
