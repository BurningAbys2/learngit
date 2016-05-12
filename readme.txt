this is a version git
demand:git init ,git add <file>,git status,git diff,git commit -m "****",
further demand:git log (查看修改日志)，or git log --pretty=oneline(一行显示)
				git reset --hard HEAD^（回退到上一个版本）or  git reset --HEAD~100(回退到上100个版本)，git reset --hard 3628164（回到指定版本号的版本，maybe newer older）
				要重返未来，用git reflog查看命令历史，以便确定要回到未来的哪个版本