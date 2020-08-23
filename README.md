根据 Git 入门教程试验的 Git 交互操作

https://www.liaoxuefeng.com/wiki/896043488029600

笔记：

- `git init`初始化一个 Git 仓库。
- `git add ‘<name>’`添加文件或`git add .`一键添加。
- `git commit -m ‘<name>’`完成。
- `git status`随时掌握工作区的状态。
- 如果有文件被修改过，用`git diff`查看修改内容。
- `HEAD`指向的版本就是当前版本。
- `git reset --hard commit_id`在版本的历史之间穿梭。
- `git log`查看提交历史，以便确定要回退到哪个版本。
- `git reflog`查看命令历史，以便确定要回到未来的哪个版本。
- `git add`实际上是把文件添加到暂存区。
- `git commit`实际上是把暂存区的所有内容提交到当前分支。
- 每次修改，如果不用`git add`到暂存区，那就不会加入到`commit`中。
- `git checkout -- file`直接丢弃工作区的修改。
- `git reset HEAD '<name>'`丢弃已添加到暂存区的修改（回到上一步）。
- `git rm`用于删除一个文件（删除文件命令）。
- `git remote add origin git@server-name:path/repo-name.git`关联一个远程库。
- `git push -u origin master`第一次推送`master`分支的所有内容。
- `git push origin master`推送此后每次最新修改。
- `git clone git@server-name:path/repo-name.git`克隆一个仓库。
- `git branch`查看分支
- `git branch <name>`创建分支
- `git checkout <name>`或者`git switch <name>`切换分支
- `git checkout -b <name>`或者`git switch -c <name>`创建+切换分支
- `git merge <name>`合并某分支到当前分支
- `git branch -d <name>`删除分支
- `git log --graph`查看分支合并图。
- `--no-ff`用普通模式合并分支，合并后的历史有分支，能看出来曾经做过合并。
- `fast forward`合并就看不出来曾经做过合并。
- `git stash`一下，然后去修复 bug。
- 修复后，再`git stash pop`，回到工作现场。
- `git cherry-pick <commit>`命令，把 bug 提交的修改“复制”到当前分支，避免重复劳动。
- `git branch -D <name>`强行删除一个没有被合并过的分支。
- `git remote -v`查看远程库信息。
- 本地新建的分支如果不推送到远程，对其他人就是不可见的。
- `git pull`抓取远程的分支，如果有冲突，要先处理冲突。
- `git push origin branch-name`从本地推送分支。
- `git checkout -b branch-name origin/branch-name`在本地创建和远程分支对应的分支。
- `git branch --set-upstream branch-name origin/branch-name`建立本地分支和远程分支的关联。
  `rebase`操作可以把本地未`push`的分叉提交历史整理成直线。
- `rebase`的目的是使得我们在查看历史提交的变化时更容易，因为分叉的提交需要三方对比。
- `git tag <tagname>`新建一个标签，默认为`HEAD`，也可以指定一个 `commit id`
- `git tag -a <tagname> -m "..."`指定标签信息。
- `git tag`查看所有标签。
- `git push origin <tagname>`推送一个本地标签。
- `git push origin --tags`推送全部未推送过的本地标签。
- `git tag -d <tagname>`删除一个本地标签。
- `git push origin :refs/tags/<tagname>`删除一个远程标签。
- 忽略某些文件时，需要编写`.gitignore`
- `.gitignore`文件本身要放到版本库里，并且可以对`.gitignore`做版本管理。
- [gitgonore](https://github.com/github/gitignore)
- `\$ git config --global **alias**.st status`
- 配置 Git 的时候，加上`--global`是针对当前用户起作用的；如果不加，那只针对当前的仓库起作用。
- 每个仓库的 Git 配置文件都放在`.git/config`文件中。
